---
layout: post
tags: [linux]
---

下载软件 http://download.csdn.net/detail/qq_21158525/9667144
或者 https://ra1nyhouse.github.io/sharedoc/xl2tpd_1.2.5+zju-1_amd64.deb

删除已经安装的xl2tpd
sudo dpkg --purge xl2tpd；sudo rm -r /etc/xl2tpd；

安装
sudo gdebi xl2tpd_1.2.5+zju-1_amd64.deb

设置账户sudo vpn-connect -c；
注意用户名格式 216****@a
连接sudo vpn-connect；
断开sudo vpn-connect -d；
