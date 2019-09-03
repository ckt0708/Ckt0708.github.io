---
title: 局部滚动和修改滚动条样式
date: 2018-09-07 09:25:00
author: 龍の蝶
img: /medias/logo.png
top: true
cover: true
coverImg: /medias/featureimages/0.jpg
password: 
toc: false
mathjax: false
summary: 这是你自定义的文章摘要内容，如果这个属性有值，文章卡片摘要就显示这段文字，否则程序会自动截取文章的部分内容作为摘要
categories: Markdown
tags:
  - 局部滚动
  - scroll-area
  - 滚动条
---
### 局部滚动和修改滚动条样式

## 部分区域滚动
代码：
```bash
//滚动条
#box{//  不滚动部分
    overflow: hidden;
    height: 100%;
}
.scroll-area{//滚动部分
    -webkit-overflow-scrolling: touch;
    overflow-y:scroll;//overflow-x 横屏滚动 overflow-y 竖屏滚动
    white-space: nowrap;
}
```

##修改滚动条样式

代码：
```python
// 改变滚动条样式
.scroll-area::-webkit-scrollbar {/*滚动条整体样式*/
	width: 10px;     /*高宽分别对应横竖滚动条的尺寸*/
	height: 1px;
}
.scroll-area::-webkit-scrollbar-thumb {/*滚动条方块*/
	border-radius: 10px;
	-webkit-box-shadow: inset 0 0 5px #ff2323;
	background: #ff2323;
}
.scroll-area::-webkit-scrollbar-track {/*滚动条里面轨道*/
	/* -webkit-box-shadow: inset 0 0 5px rgba(0,0,0,0.2); */
	/* border-radius: 10px; */
	/* background: #EDEDED; */
	border: none;
	background: none;
}
```