---
layout: post
tags: [linux, python]
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

编译完成显示

```
The necessary bits to build these optional modules were not found:
_bz2                  _curses               _curses_panel      
_dbm                  _gdbm                 _lzma              
_ssl                  readline                                 
To find the necessary bits, look in setup.py in detect_modules() for the module's name.

```

安装对应包：

实战中：
1. _ssl 使用 libssl-dev
2. readline 使用 libreadline-dev
3. _bz2 使用 libbz2-dev
4. _curses _curses_panel 使用 libncurses-dev
5. _dbm _gdbm 使用 libgdbm-dev
6. _lzma 使用 liblzma-dev

备注：

devel 包主要是供开发用，至少包括以下2个东西:
1. 头文件
2. 链接库
有的还含有开发文档或演示代码。

参考：

http://blog.csdn.net/huanle0610/article/details/41174943
