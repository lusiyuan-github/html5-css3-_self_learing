# html5-css3-_self_learing
<--关于html5/css3等前端基础自学理解-->

[TOC]



## 零. 版权声明

本文章参考b站用户：**黑马程序员pink老师**旗下视频”2黑马程序员pink老师前端入门视频教程 HTML5+CSS3+移动端布局-flex布局rem布局响应式布局摹客“总结归纳 https://www.bilibili.com/video/BV14J4114768?p=3  仅供为个人学习使用。

[^]: 下文于 2020.12.10 编写

## 一.基本知识

### (1) 网页是什么

定义：网页是构成网站的基本元素，由图片、链接、视频、文字等元素组成，因网页通常以.htm 或者.html 后缀结尾，所以俗称HTML文件。

形成：由html标签描述出来的网页元素组成，通过浏览器解析显示给用户

### (2) HTML是什么

html是一种**超文本**标记语言，是用来描述网页的语言。

注意：是标记语言而不是编程语言

标记语言是一套标记标签组成

**超文本**：

1.可以加入声音、图片、动画、多媒体等，超越文本限制。

2.可以引入超链接文本

### (3) 常用浏览器及其内核

内核（渲染引擎）：负责读取网页内容，整理信息，计算网页显示方式并显示其页面

| 浏览器       | 内核    |
| ------------ | ------- |
| IE/Edge      | Trident |
| Firefox      | Gecko   |
| Safari       | Webkit  |
| Chrome/Opera | Blink   |

国内浏览器常用内核为  Webkit/Blink

### (4) Web标准

Web标准由W3C组织和其他标准化组织制定的一系列标准的集合。

用处：符合Web标准，不同的浏览器显示相同的页面

构成：

| 标准 | 说明                                         |
| ---- | -------------------------------------------- |
| 结构 | 对网页元素进行整理分类，主要为HTML           |
| 表现 | 设置网页元素外观样式，主要为CSS              |
| 行为 | 网页模型的定义和交互的编写，主要为javascript |

Web最佳方案为：结构、表现、行为相互分离。

### (5) 开发环境

本文基于VScode开发环境编写

**安装扩展：**

open in browser 用于浏览器打开html文件

Chinese (Simplified) Language Pack for Visual Studio Code 中文包（英文大佬忽略）

Auto Rename Tag 自动重命名配对的HTML/XML标签

CSS Peek 追踪至样式

## 二. HTML

### (1) 语法规范

1.标签都要放在< > 之中，其中包含着关键词

2.标签一般成对出现叫双标签 <html>（开始标签） </html>（结束标签，多一个**反斜杠**）

3.特殊的单标签，一般单独出现，如<br />，在文字后加**空格**和**反斜杠**，此类非常少。



```html
<html> 
   <head></head>
   <body></body>
</html>

<br />
```

### (2) 标签关系

包含关系

```html
<head>
	<title></title>
</head>
```

并列关系

```html
<head></head>
<title></title>
```

### (3) html基本结构标签

```html
<html> <!--根标签-->
   <head>
       <title>lsy_self_learning</title><!--头部标题-->
   </head><!--头部标签-->
   <body>
       lsy handsome <!--文章主体-->
   </body><!--文章主体标签-->
</html>
<!--在vscode中输入“！”按下Tab键就可以导入基本骨架-->
```

[^]: 下文于 2020.12.14 编写

### (4) vscode直接生成的基本结构标签

```html
<!DOCTYPE html> 
<!--文档类型说明，使用何种html版本显示网页，不属于html标签，本句为最新html版本声明-->
<html lang="en">
<!--language = English用于定义当前文档语言，zh—CN为中文，只是定义，非强求文本内容中、英文-->
<head>
    <meta charset="UTF-8"><!--定义字符集-->  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

![image-20201214203039399](C:\Users\卢思远\AppData\Roaming\Typora\typora-user-images\image-20201214203039399.png)

<html lang="en">可以提示浏览器是否翻译

### (5) html常用标签

#### 1. 标题标签

html提供六个等级的网页标签

```html
    <h1>标题标签</h1>
    <h1>标题一共六级选,</h1>
    <h2>文字加粗一行显。</h2>
    <h3>由大到小依次减，</h3>
    <h4>从重到轻随之变。</h4>
    <h5>语法规范书写后，</h5>
    <h6>具体效果刷新见。</h6>
    　　        ------摘自pink老师
```

