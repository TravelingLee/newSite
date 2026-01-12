---
title: "GitHub重置密码出现Unable to verify your captcha response解决办法"
categories: ["GitHub"]
#externalUrl: ""
#showSummary: true
date: 2022-03-28
draft: false
---

如图，GitHub密码忘记，重置时无论用什么浏览器都显示Unable to verify your captcha response。其实我19天前遇到过同样的问题，但是忘记记录了，今天无论怎样都要记录一下。

![image.png](../img/202203281648478592660077.png)

找了网上很多办法，多是修改这个修改那个的，我觉得这事儿应该没那个难，于是我用手机试着登录了一下GitHub，然后发现了这个

![微信图片_20220328224625.jpg](../img/202203281648478810348825.jpg "微信图片_20220328224625.jpg")哈哈，不知道为什么，可能是这个验证码图片依赖Adobe Flash Player，而电脑浏览器基本都已经没有这个了，但是手机浏览器好像也没有啊，但是手机就能加载出验证码，奇了怪了。电脑因为没加载出验证码，你压根没验证，它当然不给你通过验证，所以可以换用手机试试。