# web基础

### 常见浏览器
1. IE浏览器 
2. Edge浏览器
3. 火狐浏览器（Firefox）
4. 谷歌浏览器（google Chrome）
5. Safari浏览器
6. Opera浏览器

### 浏览器内核
浏览器内核有可以分成两部分：渲染引擎（layout engineer 或者 Rendering Engine）和JS引擎。

(1). `Trident`（IE内核）
(2). `Gecko`（Firefox）
(3). `webkit`(Safari)
(4). `Chromium/Blink`(chrome)
(5). `Presto`(Opera) blink

### web标准
结构标准：结构用于对网页元素进行整理和分类，主要包括XML和XHTML两个部分。
样式标准：表现用于设置网页元素的板式、颜色、大小等外观样式，主要指CSS。
行为标准：行为是指网页模型的定义及交互的编写，主要包括DOM和ECMAScript两个部分。

# HTML入门

### HTML初识
HTML(Hyper Text Markup Language的缩写)中文译为“超文本标签语言”，主要是通过HTML标签对网页中的文本、图片、声音等内容进行描述。

### HTML骨架

```
<html>
    <head>
        <title></title>
    </head>
    <body>
    </body>
</html>
```
### 标签
在HTML页面中，带有`<>`符号的元素被称为HTML标签，如`<html>` 、`<head>` 、`<body>`等。

1. 双标签
   <标签名>内容</标签名>
   `<body></body>`
2. 单标签
   <标签名 />
   `<br />`

HTML标签：作用所有HTML中标签的一个根节点。
head标签：用于存放title，meta，base，style，script，link 注意在head标签中我们必须要设置的标签是title
body标签：页面的主体部分。
title标签：让页面拥有一个属于自己的标题.

#### 排版标签
1. 标题标签：
    `<h1><h2><h3><h4><h5><h6>`

2. 段落标签
     `<p>段落标签</p>`

3. 水平线标签
    `<hr />`

4. 换行标签
    `<br />`

5. div span 布局标签 没有语义
    `<div></div>`
    `<span></span>`

#### 文本格式化标签

~|单次|平均
---|:--:|---:
二阶|0.49|1.51
三阶|4.9|6.45


### 文档类型
```
<!DOCTYPE html>
```
这句话告诉我们使用的是html5的版本。

### 字符集
```
<meta charset="UTF-8">
```
utf-8是目前最常用的字符集编码方式。包含去世界所有国家需要用到的字符。
GB231 简单中文 ，包含6763个汉字。
BIG5 繁体中文
GBK 包含全部中文字符，是GB2312的扩展，加入对繁体字的支持，兼容GB2312。

