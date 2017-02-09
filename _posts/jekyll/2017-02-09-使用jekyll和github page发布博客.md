---
layout: post
tag: jekyll
---

jekyll是一个静态网页产生引擎，github page后台使用的就是jekyll引擎，利用github page可以简便地发布博客。

## 安装jekyll（os x）

不要使用系统自带的ruby，很容易出现问题。
os x使用homebrew安装ruby，重启终端。

```shell
brew install ruby
```

安装jekyll，和bundler:

```shell
gem install jekyll
gem install bundler
```

在[jekyllthemes](http://jekyllthemes.org/)上选择一个模板，或者直接使用`jekyll new yourblogname`生成一个博客。

如果你是在jekyllthemes上选择的模板，需要在博客目录中使用`bundler install`命令，如果出现版本不一致问题，可以尝试使用`bundler update`。

## 发布博客

注册一个github帐号，创建一个仓库以`blogname.github.io`格式命名，将blog目录push到仓库中，等待片刻，就可以用https://blogname.github.io访问了。

## 一些资源和小技巧

- 中文jekyll文档：http://jekyll.com.cn/docs/。
- jekyll category和tag的区别：tag只能在头信息中添加，category除了在头信息中添加，还会根据路径自动引入，例如`\work\_post\some.md`形式会自动添加work作为category。
- 推荐使用[多说](http://duoshuo.com/)搭建评论模块，对中文和中国社交网络支持很好。

good luck~