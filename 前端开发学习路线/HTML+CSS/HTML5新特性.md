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