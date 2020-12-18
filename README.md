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

[^]: 2020.12.16

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

#### 2. 段落换行标签

段落标签之间有较大缝隙，换行之间没有

```html
<p>段落标签</p>
<br/>换行标签
```

练习：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>体育新闻</title>
</head>
<body>
        <h1>水花61分伊戈达拉制胜抢断 西决勇士再胜开拓者总分2-0</h1>
        <h4>数据统计：水花兄弟合砍61分</h4>
       <p> 库里22投11中，三分14投4中，罚球11罚全中得到37分8篮板8助攻，职业生涯季后赛得分30+次数来到35次，超过哈登排名现役第3位，仅次于詹姆斯和杜兰特。</p>
        
       <p>汤普森22投8中，三分8投4中得到24分3篮板2助攻，德拉蒙德-格林得到16分10篮板7助攻5盖帽，凯文-鲁尼得到14分7篮板2助攻，今天勇士有7名替补出场。</p>
        
        <h4>兄弟对决升级：小库里给哥哥造成压力</h4>
        <p> 库里兄弟是NBA历史上第一对在分区决赛相遇的兄弟。在西决第1场中，小库里没有给哥哥造成压力，他出场19分钟，7投1中只得到3分3篮板2助攻，在场期间输掉10分。</p>
        
        <p>但在西决第2场中，小库里攻防两端都打出杰出的表现，全场送出4次抢断，包括直接抢断自己的哥哥库里，在防守端给库里造成了极大的困扰。</p>
        
       <p> 作者: pink老师 <br />
            2019-8-8</p>
</body>
</html>
```

#### 3.  文本格式化标签

打开word文档也会发现上面的标识也是如此

```html
<strong>加粗</strong>  <b>加粗</b>
<em>倾斜</em>			<i>倾斜</i>
<del>删除</del>		<s>删除</s>
<ins>下划线</ins>	    <u>下划线</u>
```

#### 4. div和span

两者无语义，为装内容分区，div是division缩写，表示分区、分割，span为跨度、跨距。

```html
<div>
    一个div单独占一行，相当于一个大盒子
</div>
<span>span可以一行放多个，相当于小盒子</span>
```

[^]: 2020.12.18

#### 5. 图像标签

图像标签为单标签，后续属性以空格分开

src = url存放图片路径

alt = 图像**显示不出**用文字替换

title = 鼠标放在图片上提示文本

width =   height = 设置图片宽高,当只设置其中一个时会等比例缩放

border = 设置边框粗细（一般css中指定，在图像标签时不指定）

```html
<img src="url" alt="word" title="word" width="500"  height="" border=""/>
```

#### 6. 链接标签

用于链接到另外一个页面

href="跳转目标" 

target="目标窗口弹出方式" 有 _self和 _blank两种方式，若不写，默认为 _self(当前页面打开)

href="跳转目标" 时，若目标未确定，可以写成href="#" 

```html
<a href="跳转目标" target="目标窗口弹出方式">文本或图像</a>
```

若跳转目标为网页链接，可以跳转至目标网页

若跳转目标为文件或压缩包，可以下载文件或压缩包

若跳转目标为锚点链接（在同一页面，用于快速定位）设置属性值为href = "#名字"，配合标题标签，将标题标签写入属性id = 名字，可以快速定位

```html
<a href="#one"></a>
<h3 id="one"></h3>
```

#### 7. 注释标签、特殊字符

注释标签快捷键为ctrl + l

其他特殊字符查表

![img](https://img-blog.csdnimg.cn/20190316220926880.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjM1MDIzNw==,size_16,color_FFFFFF,t_70)

```html
<!--注释标签-->
```



