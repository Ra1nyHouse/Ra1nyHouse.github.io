---
layout: post
tags: [other]
---

1. 使用xshell或者putty，实测cmder效果不好
2. 使用echo $TERM查看当前环境 8色输出为 XTERM, 256色输出为 XTERM-256color，使用tput colors输出色彩深度
3. 通常只需要在.zshrc或者.bashrc中加入export TERM='xterm-256color'即可，当前终端模拟器基本都支持256色，所以一般不需要判断是否支持256色
