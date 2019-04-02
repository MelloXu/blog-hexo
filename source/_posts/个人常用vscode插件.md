---
title: 个人常用VSCODE插件合集
date: 20180415
tags: vscode 前端 工具
---

个人常用VSCODE插件合集

<!--more-->

## 关于VSCODE ##

Visual Studio Code 是微软推出的跨平台编辑器。它采用经典的VS的UI布局，功能强大，扩展性很强。[下载地址](https://code.visualstudio.com/){:target="_blank"}

### 工具类 ###

1. [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one){:target="_blank"} (Markdown预览插件)


2. [Autoprefixer](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-autoprefixer){:target="_blank"} (自动添加css浏览器兼容前缀)


3. [IntelliSense for CSS class names in HTML](https://marketplace.visualstudio.com/items?itemName=Zignd.html-css-class-completion){:target="_blank"} (提示css类名)


4. [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag){:target="_blank"} (自动合并标签)

5. [open in browser](https://marketplace.visualstudio.com/items?itemName=techer.open-in-browser){:target="_blank"} (从浏览器中打开网页（可选择浏览器）)

6. [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense){:target="_blank"} (文件名提示)

7. [Vetur](https://marketplace.visualstudio.com/items?itemName=octref.vetur){:target="_blank"} (一个强大的vue插件,包括代码提示高亮等)

8. [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode){:target="_blank"} (强大的格式化工具)

9. [Settings Sync](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync){:target="_blank"} (同步vscode的设置和插件)


### 美化类 ###

1. [vscode-icons](https://marketplace.visualstudio.com/items?itemName=robertohuertasm.vscode-icons){:target="_blank"} (文件图标)

2. [New Moon VSCode](https://marketplace.visualstudio.com/items?itemName=taniarascia.new-moon-vscode){:target="_blank"} (主题)

3. [background](https://marketplace.visualstudio.com/items?itemName=shalldie.background){:target="_blank"} (一个很萌的代码界面背景)


### 工具使用技巧 ###
**1. Prettier - Code formatter**  
统一js风格为去掉分号，优先单引号, 设置中写入以下设置项

```javascript
"prettier.singleQuote": true, // 单引号

"prettier.semi": false // 无分号
```
**2.vscode**  
双击代码时选中范围更改,使连字符'-'可以被选中
```javascript
// 执行文字相关的导航或操作时将用作文字分隔符的字符
"editor.wordSeparators": "`~!@#$%^&*()=+[{]}\\|;:'\",.<>/?"
```