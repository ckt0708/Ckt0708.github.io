---
title: Hello World CKT My New PostMy New PostMy New PostMy New PostMy New Post
---
Welcome to [Hexo](https://hexo.io/)! This is your very first post. Check [documentation](https://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [troubleshooting](https://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/hexojs/hexo/issues).

## Quick Start 你们

### Create a new post https://github.com/ckt0708/Ckt0708.github.io.git

``` bash
hexo --save 33322222冷风机凯乐----------201908151622 201908161440
```

``` bash
$ hexo new "My New Post"
```

More info: [Writing](https://hexo.io/docs/writing.html)

### Run server

``` bash
$ hexo server
```

More info: [Server](https://hexo.io/docs/server.html)

### Generate static files

``` bash
$ hexo generate
```

More info: [Generating](https://hexo.io/docs/generating.html)

### Deploy to remote sites

``` bash
$ hexo deploy
```

More info: [Deployment](https://hexo.io/docs/deployment.html)

#局部滚动和修改滚动条样式

## 部分区域滚动
代码：
```python
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
