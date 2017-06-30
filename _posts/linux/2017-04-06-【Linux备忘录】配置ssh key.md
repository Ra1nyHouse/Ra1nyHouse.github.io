---
layout: post
tags: [linux]
---

执行如下代码

```shell
cd ~/.ssh
ssh-keygen
# id_rsa.pub 即为公钥
# 如果需要允许其他机器访问，添加文件 authorized_keys, 添加公钥即可
```


