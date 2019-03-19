---
title: mac环境变量配置
date: 2019-03-05 11:11:47
tags:
---
# mac环境变量的作用
一般mac安装完某个库时，需要执行该库命令的时候，需要进入该命令文件所在的目录下才能执行，环境变量则可以简化这一繁琐的过程，当在终端里输入某命令并敲下回车键的时候，计算机会在环境变量里指定的路径下查找这个命令对应的文件，并执行该文件以达到运行用户所需的程序。
# mac环境变量顺序
Mac系统的环境变量，加载顺序如下：

```
1. /etc/profile : 系统级别，系统启动后就会加载,建议不修改这个文件,不管是哪个用户，登录时都会读取该文件
2. /etc/paths : 系统级别，系统启动后就会加载,全局建议修改这个文件(输入环境变量时，不用一个一个地输入，只要拖动文件夹到 Terminal 里就可以了)
3. ~/.bash_profile : 用户级别，建议这里配置
4. ~/.bash_login : 用户级别
5. ~/.profile : 用户级别
6. ~/.bashrc : 用户级别，是bash shell打开的时候载入的
```
3.4.5如果优先级高的文件存在，则后面的的文件就不会读了
# mac环境变量配置
* 查看path:`echo $PATH`
* 添加path:
  `PATH="/Library/Frameworks/Python.framework/Versions/3.7/bin:${PATH}"
export PATH`,如果不想重新登录，可使用`source .bash_profile`，使该环境变量立即生效

# alias的使用
使用方法：alias 【别名】=【命令】。如果alias后面没有值，则是现实所有的命令
例如在.bash_profile中添加如下代码`alias python="/Library/Frameworks/Python.framework/Versions/3.7/bin/python3.7"`，当执行python命令是会直接链接到python3.7