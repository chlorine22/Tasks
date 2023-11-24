# Markdown原理&Typora自定义主题

> 理解Narkdown，然后搞出一个自制的好看主题:smile:

这段时间用typora敲笔记敲爽了。我本来就有写备忘录的习惯。手机自带的备忘录被我当记事本用，甚至暑假学车都用它记了几千字笔记：

![学车笔记](https://github.com/chlorine22/Tasks/blob/main/阶段3学习笔记/图片素材/xc1.jpg)

![快4000字](https://github.com/chlorine22/Tasks/blob/main/阶段3学习笔记/图片素材/xc2.jpg)

一直用一个主题很容易就会厌烦，而typora提供了五种预设主题：

![预设](https://github.com/chlorine22/Tasks/blob/main/阶段3学习笔记/图片素材/ys.png)

一般来说是够用了，但谁让我是个喜欢个性爱折腾的大学生呢:rofl:

topora也很贴心地提供了**调试功能**，基于此功能我们可以更加快速地得到我们想要的定制样式。

当然，制作自定义主题前，得先了解Markdown的原理。

## Markdown原理

Markdown编辑器本身只用于内容写作，并不支持文字排版，理论上它只是指出哪些内容是表格、哪些内容是标题、哪些是正文图片代码超链。而用于指出这些项目的符号则尽可能简单，这也使得Markdown的使用简单快捷。

Markdown 语法的目标是：**成为一种适用于网络的书写语言**，所以Markdown是兼容Html的。因此你可以将直接使用Markdown语法和Html的标签混合进行使用，因为最后都会转换成Html。

既然markdown兼容html，并且最后会转换成HTML，那就意味着，**样式表（css）同样对markdown起作用**。这也就是自定义typora主题的原理。

## Typora自定义主题

typora 是基于`electron`开发的一款软件，而且官方也提供了调试功能。

简单地说来，可以理解为 typora 其实是一个 web 应用，`electron`给它包了一个无边浏览器的壳子。

以我的版本为例，按下Shitf+F12打开开发者界面（类似网页的元素审查）：



想要自定义主题，首先得知道typora 主题本身自带的样式内容有哪些：

1. 字体样式；

![img](https://cdn.sspai.com/2020/03/13/88b5d4f9a5e92c54d057a2470d7dfda9.png?imageView2/2/w/1120/q/90/interlace/1/ignore-error/1)

2. \#write包裹的 markdown 文本编辑区域；

![img](https://cdn.sspai.com/2020/03/13/e247448c83158bd7a56f3905111c049b.png?imageView2/2/w/1120/q/90/interlace/1/ignore-error/1)

3. 编辑器侧边栏、菜单栏以及专注模式。

![img](https://cdn.sspai.com/2020/03/13/2132f5732d6ac7e943593c749a25638f.png?imageView2/2/w/1120/q/90/interlace/1/ignore-error/1)

除了样式表自带内容以外，只要你能通过 debug 方法找的界面元素，都是可以修改的。

**对于排版**，可以修改以下几个属性：

- 背景颜色：background-color
- 字体颜色：color
- 字体大小：font-size
- 行高：line-height
- 行间距：letter-spacing
- 内边距：padding
- 外边距：margin

（css字体属性和盒子属性欸）

**对于字体**，有两种方案，使用你本机安装的字体，或者下载好一些字体放在对应的目录下面。

* 本机替换的话，先找到字体英文名称，然后在开发者界面按css内部样式表语法写上，例如：

```react
body {

    font-family: KaiTi;

}
```

* 目录替换的话，下载了一个字体到本地，先定义字体名称，再使用，例如：

```react
@font-face {

    font-family: 'webfont';

    src: url('./webfont.woff') format('woff')

}

body {

    font-family: 'webfont', serif;

    color: rgb(51, 51, 51);

    line-height: 1.6;

}
```

**注意**：如果要定义中文和英文两种字体，建议**先定义英文，再中文**。因为中文字体中一般是含有字母的，那么会直接取用到中文的字体，英文效果比较差。



这两个项目自定义后，主题就基本完成了

~~下面是我的实践：~~

本来像说自己做一个的，但是做完发现好丑，还不如预设的，那还是算了吧

以后尝试慢慢做一个。

（在网上找参考时发现了一个好看的主题，[pie-dark.css](https://github.com/kevinzhao2233/typora-theme-pie/blob/master/pie-dark.css)，，分享一下:smile:）









