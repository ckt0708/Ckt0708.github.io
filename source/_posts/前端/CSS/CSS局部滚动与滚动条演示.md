---
title: 局部滚动、修改滚动条样式、隐藏滚动条
date: 2018-08-17 17:05:00
author: 龍の蝶
img: /medias/logo.png
top: true
cover: true
coverImg: /medias/featureimages/0.jpg
password: 
toc: true
mathjax: false
summary: CSS 局部滚动、修改滚动条样式、隐藏滚动条并可滚动，兼容诸多浏览器
categories: CSS
tags:
  - 局部滚动
  - 滚动条
  - 隐藏滚动条
---

## 局部滚动和修改滚动条样式

### 局部区域滚动

``` bash
/* --- 不滚动部分 --- */
.box {
    overflow: hidden;
    height: 100%;
}

/* --- 滚动部分 --- */
.scroll-area {
    -webkit-overflow-scrolling: touch;
    overflow-y:scroll;//overflow-x 横屏滚动 overflow-y 竖屏滚动
    white-space: nowrap;
}
```

### 修改滚动条样式

``` bash
/* --- 改变滚动条样式 --- */
.scroll-area::-webkit-scrollbar {
	width: 10px;
}

/* --- 滚动条里面的滚动块 灰色方块 --- */
.scroll-area::-webkit-scrollbar-thumb {
	border-radius: 10px;
	-webkit-box-shadow: inset 0 0 5px #eee;
	background: #eee;
}

/* --- 滚动条里面轨道 黄色轨道 --- */
.scroll-area::-webkit-scrollbar-track {
	-webkit-box-shadow: inset 0 0 5px rgba(0,0,0,0.2);
	border-radius: 10px;
	background: #FFEB3B;
	/* border: none;
	background: none; */
}
```

![样图](/medias/illustration/scroll.png)


### 隐藏滚动条并可滚动，兼容诸多浏览器（目前还没发现不生效的）

``` bash
/* --- webkit --- */
.scroll-area::-webkit-scrollbar {
    display: none;
}

html {
	/* --- ie --- */
	-ms-overflow-style: none;
	/* --- firefox --- */
	overflow: -moz-scrollbars-none;
}
```

![样图](/medias/illustration/scrollHidden.png)