---
layout: post
tags: [linux]
---

Driver/library version mismatch 错误原因可能是升级了cuda，导致cuda与显卡核心驱动不匹配。

注意到，我的/etc/apt/source.list.d/长这样子

```
bazel.list                                    sbt.list
bazel.list.save                               sogoupinyin.list
cuda-8-0-local.list                           typesafe-apt.list
cuda-8-0-rc.list                              webupd8team-ubuntu-java-xenial.list
graphics-drivers-ubuntu-ppa-xenial.list       webupd8team-ubuntu-java-xenial.list.save
graphics-drivers-ubuntu-ppa-xenial.list.save
```

官方deb安装包会自动创建cuda-8-0-rc.list，但是cuda-8-0-local.list总是覆盖了之前的设置，因此删掉cuda-8-0-local.list
执行下述命令

```shell
sudo apt-get purge cuda
sudo apt-get autoremove
sudo apt-get install cuda
sudo reboot
```

如果使用.sh脚本安装的cuda，在重新安装前遵照下面方法卸载原有的版本
```
To uninstall the CUDA Toolkit, run the uninstall script in /usr/local/cuda-8.0/bin
To uninstall the NVIDIA Driver, run nvidia-uninstall
```
