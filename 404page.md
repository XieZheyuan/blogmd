---
title: html 嵌入404公益页面
tags: [计算机, HTML]
date: 2020/04/07
---
大部分人在网上看到的公益404页面是如何写的呢？


其实很简单！
```html
<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <title>404 Not Found</title>

    <script type="text/javascript" src="//qzonestyle.gtimg.cn/qzone/hybrid/app/404/search_children.js" charset="utf-8" homePageUrl="自己的网站地址" homePageName="回到我的主页"></script>
</head>
<body>

<div class="footer">
    <p>Copyright © 2020自己的名字. All Rights Reserved.</p>
</div>
</body>
</html>
```

就区区13行，就实现了！

首发于CSDN博客https://blog.csdn.net/pythonbilly