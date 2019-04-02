---
title: Node.js版本管理工具
date: 20180413
tags: nodejs 前端
---

Node.js版本管理工具

<!--more-->

## node.js的安装 ##

如果你还没有安装Node.js，请先下载 [nodejs](https://nodejs.org/en/){:target="_blank"} 并安装。

如何查看Node.js和npm是否安装? 

```
$ node -v
v8.11.1

$ npm -v
5.6.0

#由于国内互联网众所周知的原因，你可以选择更换源为taobao源
$ npm set registry https://registry.npm.taobao.org/
````

## node.js的版本管理工具 ##

### 1. 使用n模块对nodejs版本进行管理 ###

`由于n不支持windows，win用户可以跳过`

n模块，是Node的一个模块，作者是TJ Holowatchuk

```
# 首先我们进行安装
$ sudo npm install -g n
```

安装完成后，直接输入n回车，会输出当前已经安装的node版本以及正在使用的版本，前面有一个o即为正在使用的版本，
你可以通过上下方向键来选择要使用的版本，回车以生效。

```
$ n
  ο node/8.11.1
    node/9.10.1
```

n的常用指令使用
```
# 安装node.js 8.9.0版本
$ n 8.9.0 

# 安装node.js最新版本
$ n latest

# 安装node.js稳定版本
$ n stable

# 删除某个版本
$ n rm 8.9.0

# 以指定的版本来执行脚本
$ n use 8.9.0 some.js

# 更多指令请使用帮助指令查看
$ n -h
```
经过n模块的版本管理后，我们可以在`/usr/local/n/versions/node/`目录下看到我们管理的node版本。

### 2. 使用nvm工具对nodejs版本进行管理 ###

> nvm是什么？nvm是一个可以让你在同一台机器上安装和切换不同版本node的工具  
> linux系统的github地址：[点我](https://github.com/creationix/nvm){:target="_blank"}  
> Mac系统的github地址：[点我](https://github.com/creationix/nvm){:target="_blank"}  
> windows-nvm的github地址： [点我](https://github.com/coreybutler/nvm-windows){:target="_blank"}  
> windows-nvm的下载地址： [下载](https://github.com/coreybutler/nvm-windows/releases){:target="_blank"}

### 开始安装(在Mac系统下) ###

打开[https://github.com/creationix/nvm](https://github.com/creationix/nvm){:target="_blank"}。
在下面的README.md中找到Install script这几个字,执行命令

**安装nvm**  
```
# 版本号会随着时间而变化，请自行在github上查看最新版本
$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh | bash
```

**添加环境变量**  
将下面的内容复制到 `.bash_profile` 文件里面，如果没有此文件则创建一个，执行 `touch .bash_profile`，
如果已经有文件则执行 `open .bash_profile`

```
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

保存文件，关闭`.bash_profile`  
更新刚配置的环境变量  
输入`source .bash_profile`

输入`nvm`，可以看到提示信息, 至此，nvm已经安装完毕

### nvm的使用 ###

```
# 查看可以安装的node版本 版本巨多故不一一列出
$ nvm ls-remote
  v8.11.1   (Latest LTS: Carbon)
   v9.0.0
   v9.1.0
   v9.2.0
   v9.2.1
   ...

# 安装指定的node版本
$ nvm install 8.9.0

# 切换使用指定的版本node
$ nvm use 8.9.0
Now using node v8.9.0 (npm v5.5.1)

# 查看当前已安装的所有node版本 
$ nvm ls

# 显示当前的版本
$ nvm current
v8.9.0

# 删除已安装的指定版本
$ nvm uninstall 8.9.0
Uninstalled node v8.9.0

# 给不同的版本号添加别名
$ nvm alias nodev1 8.9.0
nodev1 -> 8.9.0 (-> v8.9.0)

# 删除已定义的别名
$ nvm unalias nodev1
Deleted alias nodev1 - restore it with `nvm alias "nodev1" "8.9.0"`
```

**nvm 和 n 的区别**
> *nvm 类似于 Python 的 virtualenv 或者 Ruby 的 rvm ,它是一个独立安装的软件*  
> *n 其实是一个 npm 全局的开源包 ,需要使用 npm 来全局安装*  
> *n 更加轻巧,但是 nvm 更加独立.*  
> *假如你有一台新带电脑,如果你想使用 版本管理,那么 nvm 是你的选择,因为它的独立的软件,安装后你可以随意下载切换你需要的版本.*  
> *但是 n 是依赖在 npm 下的一个包,也就是说 你的电脑环境还没有 node / npm 的时候,你还用不了 n .*  
> *所以在使用的时候,大家可以针对自己的情况权衡.*

参考文章 [简书](https://www.jianshu.com/p/7eee7150e37d){:target="_blank"}