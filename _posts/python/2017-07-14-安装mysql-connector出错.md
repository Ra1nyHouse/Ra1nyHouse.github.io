---
layout: post
tags: [osx, python]
---

使用pip安装mysql-connector出错, 指出没有protobuf的include文件，原因可能是新版的mysql-connector有很多依赖包，所以使用之前的版本可以解决这个问题，推荐

```
pip install mysql-connector==2.1.4
```
