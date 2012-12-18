## 介绍
tmux是一种终端复用器，tmux是terminal muliplexer的缩写。它能够让我们在一个窗口里操作多个终端，提高我们命令行操作的效率。

## 安装
    sudo apt-get install tmux

## 基本原理
在一台Linux主机上可以启动一个tmux服务器，每个tmux服务器上可以创建多个session,一个session上可以包含多个窗口，每个窗口可以划分为多个窗格。

## 修改配置文件
在用户的主目录中可以创建一个.tmux.conf文件来配置tmux的一些行为。
1. 创建并编写配置文件    
    #改变命令的前缀,将ctrl-b改为ctrl-a以方便操作
    unbind C-b
    set -g prefix C-a
    #使用类似vi的键模式，以便于屏幕回滚和用类似于vi的操作模式编辑文本
    setw -g mode-keys vi
2. 加载配置文件
    #进入tmux拷贝模式
    ctrl-a + [
    #加载配置文件
    ：source-file ~/.tmux.conf

## 命令
1. 创建session
    tmux new-session -s name
2. 脱离当前session
    ctrl-a + d
    //关于按键的按动顺序
    * press and hold ctrl
    * press and release a
    * release ctrl
    * press and release d
3. 重新进入已经创建的session
    tmux a(ttach-session) -t name
4. 杀死某个session
    tmux kill-session -t name
5. 杀死所有session
    tmux kill-server
6. 进入tmux拷贝模式
    ctrl-a [
7. 创建新的窗口
    ctrl-a c
8. 切换到某一窗口
    ctrl-a number(窗口号)
9. 分割窗格
    to be continued ...
