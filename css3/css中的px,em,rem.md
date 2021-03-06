# 概念介绍L

1. px(pixel，像素):是一个虚拟长度单位，是计算机系统的数字化图像长度单位，如果px要换成物理长度，需要指定精度DPI(Dots Per Inch，每英寸像素数)，在扫描打印时一般有DPI可选，Windows系统默认是96dpi，Apple系统默认72dpi。像素px是相对于显示器屏幕分辨率而言的。
2. em(相对长度单位，相对于当前对象内文本的字体尺寸)：最初指字母M的宽度，现指字符宽度的倍数，用法类似百分比，如：0.8em，1.2em，2em等，通常1em=16px。相对于当前对象内文本的字体尺寸。如当前对行内文本的字体尺寸未被人为设置，则相对于浏览器的默认字体尺寸
3. pt(point,磅)：是一个物理长度单位，指的是72分之一英寸pt=1/72(英寸), px=1/dpi(英寸)
4. rem(root em,根em）是css3新增的一个相对单位，这个单位引起了广泛关注。这个单位与em有什么区别呢？区别在于使用rem为元素设定字体大小时，仍然是相对大小，但相对的只是HTML根元素。这个单位可谓集相对大小和绝对大小的优点于一身，通过它既可以做到只修改根元素就成比例地调整所有字体大小，又可以避免字体大小逐层复合的连锁反应。目前，除了IE8及更早版本外，所有浏览器均已支持rem。对于不支持它的浏览器，应对方法也很简单，就是多写一个绝对单位的声明。这些浏览器会忽略用rem设定的字体大小。
5. vw: viewpoint width,视窗宽度，1vw等于视窗宽度的1%
6. vh: viepoint height，视窗高度，1vh等于视窗高度的1%
7. vmin：vw和vh中较小的那个
8. vmax：vwhevh中较大的那个

## px的特点

1. IE无法调整那些使用px作为单位的字体大小；

2. 国外的大部分网站能够调整的原因在于其使用了em或rem作为字体单位；

3. Firefox能够调整px和em，rem，但是96%以上的中国网民使用IE浏览器(或内核)。

## em特点

1em指的是一个字体的大小，它会继承父级元素的字体大小，因此并不是一个固定的值。任何浏览器的默认字体大小都是16px。因此，12px = 0.75em。实际应用中为了方便换算，通常会如下设置样式：`html { font-size: 62.5%; }`这样，1em = 10px。我们常用的1.2em理论上就是12px。但是，这个换算在IE浏览器下不成立，1.2em会比12px稍大一些，解决办法是把html标签样式中的62.5%改成63%，

在 中文的文章中，一般会在段首空两格。如果用px作为单位，对12px字体来说需要空出24px，对14px字体来说需要空出28px......这样换算非常不通 用。如果用上em单位，这个问题就很好解决了，1个字的大小就是1em，那两个字的大小就是2em。因此，只需这样定义就行了：CSS代码`p { text-indent: 2em; }`

## rem的特点
