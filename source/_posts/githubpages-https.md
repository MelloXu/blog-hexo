---
title: 为自定义域名的Github Pages添加https支持
date: 2019/07/19
tags: 
categories: '技术'
thumbnail: /images/githubpages-https.jpg
---

首先，如果你暂时不准备购买域名，这个问题对你来说是不存在的<!--more-->，因为通过```username.github.io```进行访问的情况下 Github Pages本身已经支持https。如果你已经购买了服务器，也不需要使用本文的方法。

## 购买域名
第一步，当然是为你的博客挑选一个域名来进行绑定，这里请Google，就不多描述了，有很多域名注册商可供选择。

## 为Github Pages绑定自定义域名并开启https支持

在域名管理后台添加DNS记录映射到Github Pages ```Type: CNAME  HOSTNAME: WWW address: mellovo.github.io ```

以hexo举例，在source目录下新建文件为CNAME，没有后缀，文件内写入我们的域名。hexo g生成文件然后hexo d提交。

然后开始为我们自定义域名的Github Pages添加https支持

**虽然Github Pages早已添加了https支持，但直接用 https 链接访问自定义域名会出现证书错误（Github 提供的 SSL 证书指向的域名是*.github.com 和 *.github.io，而不是我们绑定的域名）。**

1  打开 DNS 服务商的 DNS 记录修改页面， 添加四条A Type的记录
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

ip最新地址可以在[这个页面](https://help.github.com/en/articles/setting-up-an-apex-domain#configuring-a-records-with-your-dns-provider)查看

2 保存修改后，等待 DNS 记录生效。

3 打开 GitHub Pages 设置页面，在Custom domain中填入你的域名，勾选Enforce HTTPS， 保存（如果之前已经绑定过域名的话，先清空Custom domain，然后再次绑定，原本不可勾选的Enforce HTTPS会变为可勾选。）这时会提示正在签发证书，等待证书签发成功（SSL证书由Let's Encrypt签发），此时就可以用https链接访问自定义域名了。