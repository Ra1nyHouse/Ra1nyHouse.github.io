---
layout: post
tags: [linux]
---

linux实现添加用户，几句简单命令即可：

```shell
# -d表示用户目录， -m表示自动创建目录， -s表示登录shell，-g表示主用户组，-G表示次要用户组
sudo useradd –d /home/username -m  -s /bin/sh -g group –G adm,root username

# 激活用户
sudo passwd username
```

```shell
# 删除用户-r表示删除主目录
userdel -r username
```
