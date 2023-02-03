  整理了一些经常使用的操作。

1. 检测IP是否可用
     https://www.toolsdaquan.com/ipcheck/

2. 更换IP

  甲骨文更换IP
  实例详情-附加的VNIC-VNIC详情-IP地址-更改IP地址-选择临时公共IP或者预留公共IP点击更新

  Azure更换IP
  资源组-概览(公共IP地址)-概述(取消关联)-配置(切换动静态IP)-概述(关联)（无法切换则在开新机器的时候更改ip设置)

3. 一键快速重装系统 

   重装为 Ubuntu 20.04

   ```bash
   bash <(wget --no-check-certificate -qO- 'https://raw.githubusercontent.com/MoeClub/Note/master/InstallNET.sh') -u 20.04 -v 64 -a -p "自定义root密码" -port "自定义ssh端口"
   ```


4. 安装远程桌面Xrdp

   安装Gnome桌面环境

   ```bash
   sudo apt update
   sudo apt install ubuntu-desktop
   sudo apt install xrdp 
   sudo systemctl restart xrdp
   ```

5. 甲骨文root登录

   ```bash
   sudo -i
   passwd root
   ```

   ```bash
   sudo sed -i 's/^#\?PermitRootLogin.*/PermitRootLogin yes/g' /etc/ssh/sshd_config;
   sudo sed -i 's/^#\?PasswordAuthentication.*/PasswordAuthentication yes/g' /etc/ssh/sshd_config;
   sudo service sshd restart
   ```

   甲骨文防火墙相关

   Centos

   ```bash
   systemctl stop oracle-cloud-agent
   systemctl disable oracle-cloud-agent
   systemctl stop oracle-cloud-agent-updater
   systemctl disable oracle-cloud-agent-updater
   systemctl stop firewalld.service
   systemctl disable firewalld.service
   vi /etc/selinux/config
   SELINUX=ENFORING修改成SELINUX=DISABLED
   ```

   Ubuntu

   ```bash
   iptables -P INPUT ACCEPT
   iptables -P FORWARD ACCEPT
   iptables -P OUTPUT ACCEPT
   iptables -F
   apt-get purge netfilter-persistent
   ```

6. docker快速入门

   https://docker.easydoc.net/

   


参考链接：

https://51.ruyo.net/14288.html
https://hostloc.com/thread-882460-1-1.html
https://www.moeelf.com/archives/293.html
https://www.itcoder.tech/posts/how-to-install-xrdp-on-ubuntu-20-04/
https://ednovas.xyz/2021/01/14/oraclecloud/
