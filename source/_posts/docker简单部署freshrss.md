宝塔面板安装及docker管理器安装

```bash
wget -O install.sh https://download.bt.cn/install/install-ubuntu_6.0.sh && sudo bash install.sh ed8484bec
```

安装docker-compose

```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

```bash
mkdir ~/freshrss && cd ~/freshrss
vim docker-compose.yml
```

docker-compose.yml

```yaml
version: "2.4"

volumes:
  data:
  extensions:

services:

  freshrss:
    image: freshrss/freshrss
    container_name: freshrss
    hostname: freshrss
    restart: unless-stopped
    logging:
      options:
        max-size: 10m
    ports:
      - 8989:80
    volumes:
      - ./data:/var/www/FreshRSS/data
      - ./extensions:/var/www/FreshRSS/extensions
    environment:
      CRON_MIN: '*/45'             # RSS 刷新周期，单位为分钟，*/45 表示每 45 分钟刷新一次
      TZ: Asia/Shanghai            # 时区
```

设置阅读

参考链接：

https://blog.ichr.me/post/docker-freshrss-setup/

https://dsx2016.com/?p=2859

https://www.techkoala.top/frsshrss/

[FreshRSS+RSSHub: 解决被新闻看的问题 - 少数派 (sspai.com)](https://sspai.com/post/65693)