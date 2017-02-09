---
layout: post
tags: [linux, proxy]
---

在vps或服务器上搭建代理是很常见的应用，与vpn复杂的构建不同，搭建socks5代理服务器十分简单。

## 安装

安装python，v2.7和v3.5均可，推荐2.7。使用下面命令安装：
```
pip install shadowsocks
```

要运行代理服务，使用下面命令即可：
```
sudo ssserver -p 222 -k password -m aes-256-cfb --user nobody -d start
```

封装成脚本shadow.sh：
```shell
#!/bin/zsh
if test $# -ne 1
then
    echo 'input params:start or stop'
else
   # echo $0
    if test $1 = 'start'
    then
        echo 'start server'
        sudo ssserver -p 222 -k AaA111111 -m aes-256-cfb --user nobody -d start
    else
        echo 'stop server'
        sudo ssserver -d stop
    fi
fi
```
使用`./shadow.sh start`运行代理服务， 使用`./shadow.sh stop`结束代理服务。

## 资源和小技巧

- [budgetvm](https://budgetvm.com/)是一个很棒的vps代理商，入门的vps（OpenVZ VPS）只需要25刀就可以用一年，支持支付宝支付，速度可以达到200k/s~1M/s，满足基本需求。

