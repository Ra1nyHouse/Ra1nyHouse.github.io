---
layout: post
tags: [linux]
---

首先需要iso镜像，需要easybsd

打开easybsd，在添加新条目neogrup中选择安装，点配置，拷贝下列代码

```
title Install Ubuntu
root (hd0,0)
kernel (hd0,0)/vmlinuz boot=casper iso-scan/filename=/ubuntu-14.04-desktop-i386.iso ro quiet splash locale=zh_CN.UTF-8
initrd (hd0,0)/initrd.lz
```

需要注意的是
1. 文件名记得改
2. hd0表示硬盘0，后面表示分区编号，去磁盘管理可以看到，第一个的就是0，第二个的就是1（按照那个分区图的排序）
3. 讲iso拷贝到c盘，将镜像中casper文件夹中initrd.lz vmlinuz.efs拷贝到c盘，将.disk文件夹拷贝到c盘
4. 去掉vmlinuz文件扩展名

引导进入ubuntu后，据说要
记得在这之前 要按Ctrl+Alt+T 打开终端，输入代码:sudo umount -l /isodevice这一命令取消掉对光盘所在 驱动器的挂载（注意，这里的-l是L的小写，-l 与 /isodevice 有一个空格。），否则分区界面找不到分区。
