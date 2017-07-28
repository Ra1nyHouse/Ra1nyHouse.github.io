---
layout: post
tags: [linux]
---

1. 推荐使用.sh的（run文件）安装文件，deb文件容易收到apt-get干扰，造成莫名其妙的更新
2. 安装前关闭x server,找到使用的dm，在/etc/init.d/中，我使用`sudo .lightdm stop`
3. 安装完成后，需要做一些配置，记录如下

```
Please make sure that
 -   PATH includes /usr/local/cuda-8.0/bin
 -   LD_LIBRARY_PATH includes /usr/local/cuda-8.0/lib64, or, add /usr/local/cuda-8.0/lib64 to /etc/ld.so.conf and run ldconfig as root

To uninstall the CUDA Toolkit, run the uninstall script in /usr/local/cuda-8.0/bin
To uninstall the NVIDIA Driver, run nvidia-uninstall
```

ldconfig作用

```
ldconfig命令的用途主要是在默认搜寻目录/lib和/usr/lib以及动态库配置文件/etc/ld.so.conf内所列的目录下，搜索出可共享的动态链接库（格式如lib*.so*）,进而创建出动态装入程序(ld.so)所需的连接和缓存文件。缓存文件默认为/etc/ld.so.cache，此文件保存已排好序的动态链接库名字列表，为了让动态链接库为系统所共享，需运行动态链接库的管理命令ldconfig，此执行程序存放在/sbin目录下。 ldconfig通常在系统启动时运行，而当用户安装了一个新的动态链接库时，就需要手工运行这个命令。
来自: http://man.linuxde.net/ldconfig
```
