---
title: DNS预解析
date: 2022-03-04 14:54:17
tags:
---
# DNS预解析


浏览器默认会对页面中和当前域名**不在**同一个域的域名进行预获取，并且缓存结果，这就是隐式的 DNS Prefetch。

如果想要禁用隐式的DNS prefetch ，可以使用以下的标签：

```html
< meta  http-equiv="x-dns-prefetch-control" content="off">
```

如果想对页面中**没有出现**的域进行预获取，那么就要使用显示的 DNS Prefetch 了。

```html
< link  rel="dns-prefetch" href="//www.zhix.net">
```

DNS Prefetch 应该尽量的放在网页的前面，推荐放在 `<meta charset="UTF-8">` 后面
