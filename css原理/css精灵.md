css精灵是一种网页图片应用处理方式。它允许你将一个页面涉及到的所有 零星图片都包含到一张大图中去，这样一来，当访问该页面的时候，载如的图片就不会像以前那样一副一副地慢慢显示出来了。对于当前网络的速度而言，不高于200KB的单张图片的所需载入时间基本是差不多的，所以需顾及这个问题。

CSS Sprites其实就是把网页中一些背景图片整合到一张图片文件中，再利用CSS的"background-image"，"background-repeat"，"backgound-position"的组合进行背景定位，backgound-position可以用数字精确的定位出背景图片的位置

在网页访问中，客户端需要访问一张图片都会向服务器发送请求，所以，访问的图片数量越多，请求次数也就越多，造成延迟的可能性也就越大

所以，CSS精灵技术加速的关键，并不是降低质量，而是减少个数，当然随之而来的增加内存消耗，css精灵繁琐的合成等缺点在网站性能的提升前，也就不足为道。

缺点：图片合并麻烦，维护麻烦，修改一个图片可能需要从新布局整个图片和样式

> css精灵的使用：

```
.bg_sprite{background-image:url(/整图地址); background-repeat:no-repeat}
　　　　#ico1 {width:容器宽度;height:容器高度;background-position:X坐标 Y坐标}
　　　　#ico2 {width:容器宽度;height:容器高度;background-position:X坐标 Y坐标}
　　　　#ico3 {width:容器宽度;height:容器高度;background-position:X坐标 Y坐标}
　　　　.nav {width:容器宽度;height:容器高度;background-position:X坐标 Y坐标}
```
