安装alist
docker-compose.yml

```
version: '3.3'
services:
    alist:
        restart: always
        volumes:
            - '/etc/alist:/opt/alist/data'
        ports:
            - '5244:5244'
        environment:
            - PUID=0
            - PGID=0
            - UMASK=022
        container_name: alist
        image: 'xhofe/alist-aria2:latest'
```
安装caddy 注意服务器架构
```bash
mkdir /usr/local/caddy
wget -O /usr/local/caddy/caddy "https://caddyserver.com/api/download?os=linux&arch=amd64"
chmod +x /usr/local/caddy/caddy
```

```bash
echo "https://dl.duskdust.top {
reverse_proxy 127.0.0.1:5244 {
      header_up X-Real-IP {remote_host}
      header_up X-Forwarded-Proto {scheme}
   }
}"> /usr/local/caddy/Caddyfile
```
测试caddyfile可用性
```shell
/usr/local/caddy/caddy adapt --config /usr/local/caddy/Caddyfile --validate
```

```bash
#将以下代码一起复制到SSH运行
cat > /etc/systemd/system/caddy.service <<EOF
[Unit]
Description=Caddy
Documentation=https://caddyserver.com/docs/
After=network.target network-online.target
Requires=network-online.target

[Service]
User=root
ExecStart=/usr/local/caddy/caddy run --environ --config /usr/local/caddy/Caddyfile
ExecReload=/usr/local/caddy/caddy reload --config /usr/local/caddy/Caddyfile
TimeoutStopSec=5s
LimitNOFILE=1048576
LimitNPROC=512
PrivateTmp=true
ProtectSystem=full
AmbientCapabilities=CAP_NET_BIND_SERVICE

[Install]
WantedBy=multi-user.target
EOF

#启动并设置开机自启
systemctl start caddy
systemctl enable caddy
```

参考链接：

https://www.moerats.com/archives/1034/

https://blog.ichr.me/post/docker-freshrss-setup/

https://alist.nn.ci/zh/guide/