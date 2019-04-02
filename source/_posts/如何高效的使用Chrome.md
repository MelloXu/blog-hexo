---
title: 如何高效的使用Chrome
date: 20180507
tags: 工具 浏览器 Chrome
---

一些Chrome的使用技巧和插件推荐
<!--more-->

#### 操作类 ###
**1.截图**  
Chrome本身是支持长截图以及区域截图的，那么如何进行这个操作呢？  
首先打开开发者工具 `Command + Option + I`（Windows为`F12`），随后按下`Command + Shift + P`（Windows为`Ctrl + Shift + P`），输入命令`Capture full size screenshot`，按下回车，Chrome就会自动截取整个网页内容并保存至本地，由于是渲染引擎直接输出，其比普通扩展速度更快，分辨率也更高。  
区域截图  
有时候你需要截取一个版块或者一个按钮的图像，使用QQ等工具总是不太方便，Chrome支持根据DOM节点来截图，打开开发者工具（操作同上），在Elements选项卡下用鼠标选择你要截取的DOM内容并点下，按下`Command + Shift + P`，输入命令`Capture node screenshot`，Chrome就会自动截取你所选取的DOM节点的内容。

**2. 显示fps和资源占用**  
打开开发者工具，按下`Command + Shift + P`，输入命令`Show Rendering`,按下回车，开发者工具下方会出现一个Rendering的选项卡，勾选FPS meter这个选项，在页面右上角会出现一个统计浮层，实时显示当前页面的fps和GPU的占用。

**3. 打开Shadow DOM显示**  
通过配置能够在元素标签器中显示被隐藏的组件代码  
Settings → General → Elements → Show user agent shadow DOM


### 插件 ###

**[插件crx文件下载网站https://chrome-extension-downloader.com/](https://chrome-extension-downloader.com/)**

**1. Adblock Plus**  
[Adblock Plus](https://chrome.google.com/webstore/detail/adblock-plus/cfhdojbkjhnklbpkdaibdccddilifddb)  
Adblock Plus 是世界上最流行的浏览器扩展，世界各地有数百万用户在使用它。这是一个社区驱动的开源项目，有数百名志愿者为 Adblock Plus 的成功作出了贡献，以实现所有烦人的广告被自动阻挡，不仅如此，你还可以手动对网页上的元素进行拦截。

**2. Tampermonkey**
[Tampermonkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)  
Tampermonkey 是一款免费的浏览器扩展和最为流行的用户脚本管理器，它适用于 Chrome, Microsoft Edge, Safari, Opera Next, 和 Firefox。 推荐使用[Greasy Fork](https://greasyfork.org/)来寻找和安装脚本

**3.Allow-Control-Allow-Origin**  
[Allow-Control-Allow-Origin](https://chrome.google.com/webstore/detail/allow-control-allow-origi/nlfbmbojpeacfghkpbjhddihlkkil)  
Allow-Control-Allow-Origin可以使你在开发时跨域获取数据，

**4. jsonView**  
[jsonView jsonViewer json formatter 格式化](https://chrome.google.com/webstore/detail/jsonview-jsonviewer-json/hdmbdioamgdkppmocchpkjhbpfmpjiei)  
对json文件进行格式化，支持 json 和 jsonp 格式，显示链接和图片预览

**5. EditThisCookie**  
[EditThisCookie](https://chrome.google.com/webstore/detail/editthiscookie/fngmhnnpilhplaeedifhccceomclgfbg)  
EditThisCookie是一个cookie管理器。您可以添加，删除，编辑，搜索，锁定和屏蔽cookies！

**6. Wappalyzer**  
[Wappalyzer](https://chrome.google.com/webstore/detail/wappalyzer/gppongmhjkpfnbhagpmjfkannfbllamg)  
Wappalyzer可以查看网站所使用的技术语言等。

**7. Restlet Client - REST API Testing**

[Restlet Client - REST API Testing](https://chrome.google.com/webstore/detail/restlet-client-rest-api-t/aejoelaoggembcahagimdiliamlcdmfm)

在线进行get post等接口数据操作