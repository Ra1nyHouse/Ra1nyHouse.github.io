---
layout: post
tags: [linux, homebrew]
---
官网下载源码包

```shell
./configure --prefix=/home/house/opt/python # 安装地址
make # 编译
make install # 安装
```
报错
INFO: Can't locate Tcl/Tk libs and/or headers

解决方法， 后缀dev 使得包含头文件

```
apt-get install tcl-dev    
apt-get install tk-dev 
```

报没权限错误，通常需要进到相应目录，给configure文件赋执行权限

```
chmod u+x configure
```

