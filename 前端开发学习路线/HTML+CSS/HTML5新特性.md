#  HTML新特性

## 音频
### 1、Audio（音频）
HTML5提供了播放音频文件的标准

### 2、control（控制器）
control属性提供添加播放、暂停和音量控件

### 3、标签
`<audio>`  定义声音
`<source>` 规定多媒体资源，可以是多个

例子：`<audio src="1.mp3" controls="controls">浏览器不支持 </audio>`

```
<audio controls="controls">
    <source src="raw/3.mp4">
    <source src="raw/3.ogg">
</audio>
```


## HTML5视频
### 1、video（视频）
HTML5提供了展示视频的标准
### 2、control（控制器）
control属性供添加播放、暂停和音量控件
### 3、标签：
`<video>` 定义声音
`<source>`规定多媒体资源，可以是多个

###  4、属性
width：宽
height：高

例子：`<video src="raw/3.mp4" controls="controls" height="300px" width="300px">浏览器不支持</video>`
```
<video src="raw/3.mp4" controls="controls" height="300px" width="300px">
    <source src="raw/3.mp4">
</video>
```

## HTML拖放
拖放：是一种常见的特性，抓取对象以后拖到另一个位置。
浏览器支持:ie9 firefox opera12 chrome safari.
设置元素为可拖放：draggable="true"
拖动什么：ondragstart和setData()
放到何处：ondragover
进行放置：ondrop

例子：
```
<style>
#div1{
    width:300px;
    height:300px;
    border:1px solid #aaabbb
}
</style>
<script>
function allowDrop (ev){
    ev.preventDefault();
}
//放置
function drag(ev){
    ev.dataTransfer.setData("Text",ev.target.id);
}
// 拖动
function drop(ev){
    ev.preventDefault();
    var data = ev.dataTransfer.getData("Text");
    ev.target.appendChild(document.getElementById(data));
}
</script>
<div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)">
</div>
<img id="drag1" src="images/1/png" draggable="true" ondragstart="drag(event)"/>
```


### 画布
画布：是一个矩形区域，您可以控制其每一个像素
canvas 拥有多种绘制路径、矩形、圆形、字符以及添加图像的方法。

### SVG
##### 什么是SVG？
SVG 指可伸缩矢量图形（Scalable Vector Graphics）
SVG用于定义用于网络的机遇矢量的图形
SVG使用XML格式定义图形
SVG图像在放大或改变尺寸的情况下其图形质量不会有损失
SVG是万维网联盟标准
##### SVG的优势
与其他图像城市相比（比如jpeg和GIF），使用svg的优势在与
svg图像可通过文本编辑器来创建和修改
svg图像可被搜索、索引、脚本化或压缩
svg是可伸缩的
svg可在图像质量不下降的情况下被放大
##### 浏览器支持
IE9 Firefox Opera Chrome以及Safari 

##### svg的创建
<svg viewbox="0 0 120 120" version="1.1" xmls="http://www.w3.org/2000/svg">
<cricle cx=""/>
</svg>