---
layout: post
tags: [linux]
---

打开tmux终端直接使用`tmux`即可
改session名字使用`C-b $`

显示所有session

```
tmux ls
```

进入session

```
tmux attach -t session_name
```

detach session使用`C-b d`

解决emacs显示色彩异常：

在 ~/.tmux.conf 文件中写入 set -g default-terminal "screen-256color" 即可。
解决nvim alt（meta）不响应： set -s escape-time 0

# 支持鼠标
# set-window-option -g mode-mouse on
# setw -g aggressive-resize on

其他命令

```
brew install tmux    #安装tmux
tmux attach   #可以当启动tmux使用- -.
tmux new-session -s rails  #创建rails 会话
tmux new-session -s rails -d   #在后台创建rails
tmux list-sessions / tmux ls   #列出所有正在运行的会话
tmux a -t rails #进入rails 会话
tmux kill-session -t rails   #关闭rails 会话
tmux kill-server   #关闭tmux服务，所有的会话将被关闭
tmux 的快捷键，常见的操作：
Ctrl B  d  #隐藏会话
Ctrl B  c   #新开一个窗口
Ctrl B   &   #退出当前窗口
Ctrl B  ，  #重命名窗口
Ctrl B   数字     #切换到第几个窗口
Ctrl B   n     #切换到下个窗口
Ctrl B  p     #切换到上个窗口
Ctrl B   l       #切换到最后一个窗口
Ctrl B    w    #以菜单的方式显示和选择窗口
Ctrl B  ”       #横向分割窗口
Ctrl B  %       #纵向分割窗口
Ctrl B   o      #跳到下一个分割窗口
Ctrl B   上下左右    #跳到指定方向的分割窗口
Ctrl B    x    #关闭当前分割窗口
Ctrl B   ！    #关闭所有分割窗口
C Ctrl-方向键   #调整分割窗口大小
Ctrl B   ？  显示快捷键帮助
Ctrl B   t    显示时钟
Ctrl B  [     #进入拷贝模式，可以使用上下左右键或者触摸板来翻页，Ctrl + C 退出
Ctrl B  ]      #粘贴
Ctrl B space   #开始复制（拷贝模式）


tmux #开启tmux    
tmux ls #显示已有tmux列表（C-b s）    
tmux attach-session -t 数字 #选择tmux    
C-b c 创建一个新的窗口    
C-b n 切换到下一个窗口    
C-b p 切换到上一个窗口    
C-b l 最后一个窗口,和上一个窗口的概念不一样哟,谁试谁知道    
c-b w 通过上下键选择当前窗口中打开的会话    
C-b 数字 直接跳到你按的数字所在的窗口    
C-b & 退出当前窗口    
C-b d 临时断开会话 断开以后,还可以连上的哟:)    
C-b " 分割出来一个窗口    
C-b % 分割出来一个窗口    
C-b o 在小窗口中切换    
C-b (方向键)    
C-b ! 关闭所有小窗口    
C-b x 关闭当前光标处的小窗口    
C-b t 钟表  
```
