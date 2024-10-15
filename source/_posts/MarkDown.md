---
title: MarkDown
date: 2023-10-17 16:08:09
tags: [语法,计算机]
---

# MarkDown语法
本条记录一些用markdown书写过程中遇到的一些官方文档中未找到的问题
 <!-- more -->

1. [居中问题](#1居中问题)
2. [字体问题](#2字体问题)
3. [缩进问题](#3缩进问题)
4. [页面内部跳转](#4页面内部跳转)

## 1、居中问题

markdown语法本身并不能直接设置居中，但markdown文件支持html语法，所以直接利用html语法居中文字及图片。

    图片居中
    <div align="center"> <img src="图片地址" width = 500 height = 300 /> </div>
    文字居中
    <center>居中文字</center>

如下为显示效果:
<div align="center"> <img src="MarkDown/example_picture.png" width = 500 height = 300 /> </div>
<center>Example Picture</center>

## 2、字体问题
markdown语法本身也不支持字体改变，所以也需要使用html语法

### 改变字体大小
```html
<font size=1>字体大小size=1</font>
<font size=3>字体大小size=3</font>
<font size=5>字体大小size=5</font>
```
使用参数 **size** 。可取值为1-7

如下为显示效果
<font size=1>字体大小size=1</font>
<font size=3>字体大小size=3</font>
<font size=5>字体大小size=5</font>

### 改变字体颜色

1、英文字母
```html
<font color=red>红色</font>
<font color="blue">蓝色</font>
<font color=Yellow>黄色</font>
<font color=YellowGreen>黄绿色</font>
```
显示效果
<font color=red>红色</font>
<font color="blue">蓝色</font>
<font color=Yellow>黄色</font>
<font color=YellowGreen>黄绿色</font>

2、十六进制编码
```html
<font color=#ff0000>红色</font>
<font color=#00ff00>绿色</font>
<font color=#0000ff>蓝色</font>
<font color=#dc9fb4>抚子</font>
```
<font color=#ff0000>红色</font>
<font color=#00ff00>绿色</font>
<font color=#0000ff>蓝色</font>
<font color=#dc9fb4>抚子</font>

使用参数**color**。更推荐十六进制颜色显示，对于一些不常见的颜色有很好的适应性，并且还可以依据个人喜好改变RGB选择自己喜欢的颜色。英文表示更加简单易用，记住常见的几种颜色英文即可。

### 改变字体类型

```html
<font face="黑体">黑体</font>
<font face="宋体">宋体</font>
<font face="仿宋">仿宋</font>
<font face="幼圆">幼圆</font>
<font face="楷书">楷书</font>
<font face="华文行楷">华文行楷</font>
<font face="华文隶书">华文隶书</font>
<font face="华文新魏">华文新魏</font>
<font face="华文彩云">华文彩云</font>
<font face="华文琥珀">华文琥珀</font>
```

显示效果如下所示
<font face="黑体">黑体</font>
<font face="宋体">宋体</font>
<font face="仿宋">仿宋</font>
<font face="幼圆">幼圆</font>
<font face="楷书">楷书</font>
<font face="华文行楷">华文行楷</font>
<font face="华文隶书">华文隶书</font>
<font face="华文新魏">华文新魏</font>
<font face="华文彩云">华文彩云</font>
<font face="华文琥珀">华文琥珀</font>

使用参数**face**。注意，字体类型的设置只能在电脑上才能显示字体效果，在手机上无法显示字体类型。

```html
<font size=5 color=red face="华文彩云">华文彩云</font>
```

<font size=5 color=blue face="宋体">宋体</font>

混合使用时注意参数之间加上空格。

## 3、缩进问题

``` html
    &ensp; or &#8194;   表示一个半角的空格
    &emsp; or &#8195;   表示一个全角的空格
    &emsp;&emsp;        两个全角的空格（用的比较多）
    &nbsp; or &#160;    不断行的空白格
```

如下为显示效果
&ensp;示例文字
&emsp;示例文字
&emsp;&emsp; 示例文字
&nbsp;示例文字

## 4、页面内部跳转

```markdown
    [文本内容](#需要跳转的标题)
```
示例如下，可以跳转到本文的第一个标题
[居中问题](#1居中问题)
