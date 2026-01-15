---
title: "博客园底部添加音乐播放器"
tags: ["建站", "前端"]
categories: ["前端"]
#externalUrl: ""
showSummary: true
summary: "根据目前（2022-05-12）最新的APlayer和MetingJS进行编写的，示例来自MetingJS的GitHub项目"
date: 2022-05-12
draft: false
---


根据目前（2022-05-12）最新的APlayer和MetingJS进行编写的，示例来自MetingJS的GitHub项目，项目地址：<a>https://github.com/metowolf/MetingJS/tree/master</a>
![](../img/202205121921219143744.png)
在博客园后台的页脚代码中添加如下代码：

```html
<!-- require APlayer -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/aplayer/dist/APlayer.min.css">
<script src="https://cdn.jsdelivr.net/npm/aplayer/dist/APlayer.min.js"></script>
<!-- require MetingJS -->
<script src="https://cdn.jsdelivr.net/npm/meting@2/dist/Meting.min.js"></script>

<meting-js
	server="netease"
	type="playlist"
	mini="true"
	fixed="true"
	id="2846803618">
</meting-js>
```

![](../img/202205121921466301558.png)
这里是引用网易云的歌单，server就是指定音乐平台；这里的id是网易云歌单id，你可以换成你自己喜欢的歌单。除了歌单，你也可以添加单首歌，改变type属性的参数即可。
关于MetingJS的属性，请访问MetingJS的GitHub页面，参考官方文档。

