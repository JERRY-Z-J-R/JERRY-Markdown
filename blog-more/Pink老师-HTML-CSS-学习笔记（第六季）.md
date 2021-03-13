---
title: Pink老师 HTML CSS 学习笔记（第六季）
date: 2021-01-21 20:16:21
categories:
- [前端]
- [HTML]
- [CSS]
tags:
- HTML
- CSS
- Pink
---

![](https://img-blog.csdnimg.cn/20210116002056446.jpg)

<!--more-->

> 本学习笔记是个人对Pink老师课程的总结归纳，转载请注明出处！ 

# Pink老师 HTML CSS 学习笔记（第六季）

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Pink老师 HTML CSS 学习笔记（第六季）](#pink%E8%80%81%E5%B8%88-html-css-%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%E7%AC%AC%E5%85%AD%E5%AD%A3)
- [CSS 盒子模型](#css-%E7%9B%92%E5%AD%90%E6%A8%A1%E5%9E%8B)
  - [1、看透网页布局的本质](#1%E7%9C%8B%E9%80%8F%E7%BD%91%E9%A1%B5%E5%B8%83%E5%B1%80%E7%9A%84%E6%9C%AC%E8%B4%A8)
  - [2、盒子模型（Box Model）组成](#2%E7%9B%92%E5%AD%90%E6%A8%A1%E5%9E%8Bbox-model%E7%BB%84%E6%88%90)
  - [3、边框（border）](#3%E8%BE%B9%E6%A1%86border)
  - [4、表格的细线边框](#4%E8%A1%A8%E6%A0%BC%E7%9A%84%E7%BB%86%E7%BA%BF%E8%BE%B9%E6%A1%86)
  - [5、边框会影响盒子实际大小](#5%E8%BE%B9%E6%A1%86%E4%BC%9A%E5%BD%B1%E5%93%8D%E7%9B%92%E5%AD%90%E5%AE%9E%E9%99%85%E5%A4%A7%E5%B0%8F)
  - [6、内边距（padding）](#6%E5%86%85%E8%BE%B9%E8%B7%9Dpadding)
  - [7、外边距（margin）](#7%E5%A4%96%E8%BE%B9%E8%B7%9Dmargin)
  - [8、外边距合并](#8%E5%A4%96%E8%BE%B9%E8%B7%9D%E5%90%88%E5%B9%B6)
    - [a、相邻块元素垂直外边距的合并](#a%E7%9B%B8%E9%82%BB%E5%9D%97%E5%85%83%E7%B4%A0%E5%9E%82%E7%9B%B4%E5%A4%96%E8%BE%B9%E8%B7%9D%E7%9A%84%E5%90%88%E5%B9%B6)
    - [b、嵌套块元素垂直外边距的塌陷](#b%E5%B5%8C%E5%A5%97%E5%9D%97%E5%85%83%E7%B4%A0%E5%9E%82%E7%9B%B4%E5%A4%96%E8%BE%B9%E8%B7%9D%E7%9A%84%E5%A1%8C%E9%99%B7)
  - [9、清除内外边距](#9%E6%B8%85%E9%99%A4%E5%86%85%E5%A4%96%E8%BE%B9%E8%B7%9D)
  - [10、案例](#10%E6%A1%88%E4%BE%8B)
  - [11、Pink 老师总结](#11pink-%E8%80%81%E5%B8%88%E6%80%BB%E7%BB%93)
    - [a、布局为啥用不同盒子,我只想用 div？](#a%E5%B8%83%E5%B1%80%E4%B8%BA%E5%95%A5%E7%94%A8%E4%B8%8D%E5%90%8C%E7%9B%92%E5%AD%90%E6%88%91%E5%8F%AA%E6%83%B3%E7%94%A8-div)
    - [b、为啥用辣么多类名？](#b%E4%B8%BA%E5%95%A5%E7%94%A8%E8%BE%A3%E4%B9%88%E5%A4%9A%E7%B1%BB%E5%90%8D)
    - [c、到底用 margin 还是 padding？](#c%E5%88%B0%E5%BA%95%E7%94%A8-margin-%E8%BF%98%E6%98%AF-padding)
    - [d、自己做没有思路？](#d%E8%87%AA%E5%B7%B1%E5%81%9A%E6%B2%A1%E6%9C%89%E6%80%9D%E8%B7%AF)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->



> 原创思维导图，开源地址：https://github.com/JERRY-Z-J-R/JERRY-Mind

![](https://img-blog.csdnimg.cn/20210219021506627.png)

# CSS 盒子模型

页面布局要学习三大核心, 盒子模型, 浮动 和 定位。学习好盒子模型能非常好的帮助我们布局页面

## 1、看透网页布局的本质

网页布局过程：

- 先准备好相关的网页元素，网页元素基本都是盒子 Box 

- 利用 CSS 设置好盒子样式，然后摆放到相应位置

- 往盒子里面装内容

网页布局的核心本质： 就是利用 CSS 摆盒子

## 2、盒子模型（Box Model）组成

所谓 盒子模型：就是把 HTML 页面中的布局元素看作是一个矩形的盒子，也就是一个盛装内容的容器
CSS 盒子模型本质上是一个盒子，封装周围的 HTML 元素，它包括：`边框`、`外边距`、`内边距`、和 `实际内容`

![](https://img-blog.csdnimg.cn/20210125235703118.jpg)

## 3、边框（border）

`border` 可以设置元素的边框。边框有三部分组成：`边框宽度(粗细)`、`边框样式`、`边框颜色`

语法：

```css
border : border-width || border-style || border-color
```

| 属性           | 作用                      |
| -------------- | ------------------------- |
| `border-width` | 定义边框粗细，单位是 `px` |
| `border-style` | 边框的样式                |
| `border-color` | 边框颜色                  |

CSS 边框属性允许你指定一个元素边框的样式和颜色。

语法：

```css
border : border-width || border-style || border-color
```

边框样式 border-style 可以设置如下值：

- `none`：没有边框即忽略所有边框的宽度（默认值）
- `solid`：边框为单实线（最为常用的）
- `dashed`：边框为虚线
- `dotted`：边框为点线

边框简写：

```css
border: 1px solid red; 没有顺序
```

边框分开写法：

```css
border-top: 1px solid red; 		/* 只设定上边框， 其余同理 */
```

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>盒子模型之边框的复合写法</title>
    <style>
        div {
            width: 300px;
            height: 200px;
            /* 
            -- border-width 边框的粗细，一般情况下使用 px --
            border-width: 5px;
            -- border-width 边框的样式 solid 实线边框 dashed 虚线边框 dotted 点线边框 --
            border-style: solid;
            background-color: pink;
            */
            /* 边框的复合写法 简写： */
            border: 5px solid pink;
            /* 利用CSS层叠性将上边框单独覆盖 */
            border-top: 5px solid green;
        }
    </style>
</head>

<body>
    <div></div>
</body>

</html>
```



## 4、表格的细线边框

border-collapse 属性控制浏览器绘制表格边框的方式。它控制相邻单元格的边框

语法：

```css
border-collapse:collapse;
```

- `collapse` 单词是合并的意思
- `border-collapse: collapse;` 表示相邻边框合并在一起

## 5、边框会影响盒子实际大小

边框会额外增加盒子的实际大小。因此我们有两种方案解决:

- 测量盒子大小的时候,不量边框
- 如果测量的时候包含了边框,则需要 width / height 减去边框宽度

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>盒子模型之利用盒子模型改变表格的边框</title>
    <style>
        table {
            width: 500px;
            height: 249px;
        }

        th {
            height: 35px;
        }

        table,
        td,
        th {
            border: 1px solid pink;
            /* 合并相邻的边框, 如果不这样做，那么单元格边框会叠加变为两倍宽 */
            border-collapse: collapse;
            font-size: 14px;
            text-align: center;
        }
    </style>
</head>

<body>
    <!-- align cellspacing 的 CSS 方式修改后面再讨论 -->
    <table align="center" cellspacing="0">
        <thead>
            <tr>
                <th>12345</th>
                <th>12345</th>
                <th>12345</th>
                <th>12345</th>
                <th>12345</th>
                <th>12345</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
            </tr>
            <tr>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
            </tr>
            <tr>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
            </tr>
            <tr>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
            </tr>
            <tr>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
            </tr>
            <tr>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
                <td>12345</td>
            </tr>
    </table>
</body>

</html>
```



## 6、内边距（padding）

padding 属性用于设置内边距，即边框与内容之间的距离

| 属性             | 作用     |
| ---------------- | -------- |
| `padding-left`   | 左内边距 |
| `padding-rigth`  | 右内边距 |
| `padding-top`    | 上内边距 |
| `padding-bottom` | 下内边距 |

padding 属性（简写属性）可以有一到四个值

| 值的个数                       | 表达意思                                                   |
| ------------------------------ | ---------------------------------------------------------- |
| `padding: 5px;`                | 1个值，代表上下左右都有5像素内边距;                        |
| `padding: 5px 10px;`           | 2个值，代表上下内边距是5像素，左右内边距是10像素           |
| `padding: 5px 10px 20px;`      | 3个值，代码上内边距5像素，左右内边距10像素，下内边距20像素 |
| `padding: 5px 10px 20px 30px;` | 4个值，上是5像素 右10像素 下20像素 左是30像素 顺时针       |

以上 4 种情况，我们实际开发都会遇到

当我们给盒子指定 `padding` 值之后，发生了 2 件事情：

- 内容和边框有了距离，添加了内边距
- `padding` 影响了盒子实际大小

也就是说，如果盒子已经有了宽度和高度，此时再指定内边框，会撑大盒子

解决方案：

如果保证盒子跟效果图大小保持一致，则让 width / height 减去多出来的内边距大小即可

如何盒子本身没有指定 width / height 属性, 则此时 padding 不会撑开盒子大小

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>盒子模型之内边距</title>
    <style>
        div {
            width: 200px;
            height: 200px;
            background-color: pink;
            /*
            padding-top: 5px;
            padding-rigth: 10px;
            padding-bottom: 20px;
            padding-rigth: 30px;
             */
            /* 内边距复合写法（简写） 上、右、下、左 */
            padding: 5px 10px 20px 30px;
        }
    </style>
</head>

<body>
    <div>
        盒子内容是 content，盒子内容是 content，盒子内容是 content
    </div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210125235703635.png)

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>新浪导航案例-padding影响盒子的好处</title>
    <style>
        .nav {
            height: 41px;
            border-top: 3px solid #ff8500;
            border-bottom: 1px solid #edeef0;
            background-color: #fcfcfc;
            line-height: 41px;
        }

        .nav a {
            /* a 属于行内元素 此时必须要转换 行内块元素 */
            display: inline-block;
            height: 41px;
            padding: 0 20px;
            font-size: 12px;
            color: #4c4c4c;
            text-decoration: none;
        }

        .nav a:hover {
            background-color: #eee;
            color: #ff8500;
        }
    </style>
</head>

<body>
    <div class="nav">
        <a href="#">设为首页</a>
        <a href="#">手机新浪网</a>
        <a href="#">移动客户端</a>
        <a href="#">登录</a>
        <a href="#">微博</a>
        <a href="#">博客</a>
        <a href="#">邮箱</a>
        <a href="#">网站导航</a>
    </div>
</body>

</html>
```

```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>简洁版小米侧边栏案例-padding影响盒子大小计算</title>
    <style>
        /* 1、把 a 转换为块级元素 */
        a {
            display: block;
            width: 200px;
            height: 40px;
            background-color: #55585a;
            font-size: 14px;
            color: #fff;
            text-decoration: none;
            padding-left: 30px;
            /* 一个小技巧：单行文字垂直居中的代码，让文字的行高等于盒子的高度 */
            line-height: 40px;
        }

        /* 2、鼠标经过链接变换背景颜色 */
        a:hover {
            background-color: #ff6700;
        }
    </style>
</head>

<body>
    <a href="#">手机 电话卡</a>
    <a href="#">电视 盒子</a>
    <a href="#">笔记本 平板</a>
    <a href="#">出行 穿戴</a>
    <a href="#">智能 路由器</a>
    <a href="#">健康 儿童</a>
    <a href="#">耳机 音响</a>
</body>

</html>
```



## 7、外边距（margin）

`margin` 属性用于设置外边距，即控制盒子和盒子之间的距离

| 属性            | 作用     |
| --------------- | -------- |
| `margin-left`   | 左外边距 |
| `margin-right`  | 右外边距 |
| `margin-top`    | 上外边距 |
| `margin-bottom` | 下外边距 |

`margin` 简写方式代表的意义跟 `padding` 完全一致

外边距典型应用

外边距可以让块级盒子水平居中，但是必须满足两个条件：

- 盒子必须指定了宽度（width）
- 盒子左右的外边距都设置为 `auto`

```css
.header{ width:960px; margin:0 auto;}
```

常见的写法，以下三种都可以：

- `margin-left: auto; margin-right: auto;`
- `margin: auto;`
- `margin: 0 auto;`

注意：以上方法是让块级元素水平居中，行内元素或者行内块元素水平居中给其父元素添加 `text-align:center` 即可

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>盒子模型之外边距margin</title>
    <style>
        div {
            width: 200px;
            height: 200px;
            background-color: pink;
        }

        /* 
        .one {
            margin-bottom: 20px;
        } 
        */
        
        .two {
            margin-top: 20px;
        }
    </style>
</head>

<body>
    <div class="one">1</div>
    <div class="two">2</div>
</body>

</html>
```

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>块级盒子水平居中对齐</title>
    <style>
        .header {
            width: 900px;
            height: 200px;
            background-color: pink;
            /* 上下 100 左右 auto */
            margin: 100px auto;
        }
    </style>
</head>

<body>
    <div class="header"></div>
</body>

</html>
```

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>行内元素 / 行内块元素水平居中对齐</title>
    <style>
        .header {
            width: 900px;
            height: 200px;
            background-color: pink;
            margin: 100px auto;
            /* 行内元素或者行内块元素水平居中给其父元素添加 text-align: center 即可 */
            text-align: center;
        }

        /* 这样是不起作用的 */
        /* 
        span {
            margin: 0 auto;
        } 
        */
    </style>
</head>

<body>
    <div class="header">
        <span>里面的文字</span>
    </div>
    <div class="header">
        <img src="../image/icon.png" alt="">
    </div>
</body>

</html>
```



## 8、外边距合并

使用 `margin` 定义块元素的垂直外边距时，可能会出现外边距的合并

主要有两种情况:

- 相邻块元素垂直外边距的合并
- 嵌套块元素垂直外边距的塌陷

### a、相邻块元素垂直外边距的合并

当上下相邻的两个块元素（兄弟关系）相遇时，如果上面的元素有下外边距 `margin-bottom`，下面的元素有上外边距 `margin-top` ，则他们之间的垂直间距不是 `margin-bottom` 与 `margin-top` 之和。取两个值中的较大者这种现象被称为相邻块元素垂直外边距的合并

![](https://img-blog.csdnimg.cn/20210125235708444.png)

解决方案：

尽量只给一个盒子添加 `margin` 值

### b、嵌套块元素垂直外边距的塌陷

对于两个嵌套关系（父子关系）的块元素，父元素有上外边距同时子元素也有上外边距，此时父元素会塌陷较大的外边距值

![](https://img-blog.csdnimg.cn/20210125235708442.png)

解决方案：

- 可以为父元素定义上边框
- 可以为父元素定义上内边距
- 可以为父元素添加 `overflow: hidden`

还有其他方法，比如浮动、固定，绝对定位的盒子不会有塌陷问题，后面咱们再总结

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>外边距合并-嵌套块级元素垂直外边距塌陷</title>
    <style>
        .father {
            width: 400px;
            height: 400px;
            background-color: purple;
            margin-top: 50px;
            /* border: 1px solid red; */
            /* border: 1px solid transparent; */
            /* padding: 1px; */
            overflow: hidden;
        }

        .son {
            width: 200px;
            height: 200px;
            background-color: pink;
            margin-top: 100px;
        }
    </style>
</head>

<body>
    <div class="father">
        <div class="son"></div>
    </div>
</body>

</html>
```



## 9、清除内外边距

网页元素很多都带有默认的内外边距，而且不同浏览器默认的也不一致。因此我们在布局前，首先要清除下网页元素的内外边距

```css
* {
	padding:0; 	/* 清除内边距 */
	margin:0; 	/* 清除外边距 */
}
```

注意：行内元素为了照顾兼容性，尽量只设置左右内外边距，不要设置上下内外边距。但是转换为块级和行内块元素就可以了

## 10、案例

```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>综合案例-小米商城产品模块</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }

        body {
            background-color: #f5f5f5;
        }

        a {
            color: #333;
            text-decoration: none;
        }

        .box {
            width: 298px;
            height: 415px;
            background-color: #fff;
            margin: 100px auto;
            text-align: center;
        }

        .box img {
            margin: 0 auto;
        }

        .review {
            height: 56px;
            font-style: 14px;
            /* 因为这个段落没有 width 属性，所以 padding 不会撑开盒子的宽度 */
            padding: 0 28px;
            margin-top: 15px;
        }

        .appraise {
            font-style: 12px;
            color: #b0b0b0;
            margin-top: 15px;
            padding: 0 28px
        }

        .info {
            font-style: 14px;
            margin-top: 15px;
            padding: 0 28px;
        }

        .info h4 {
            display: inline-block;
            font-weight: 400;
        }

        .info span {
            color: #ff6700;
        }

        .info em {
            font-style: normal;
            color: #ebe4e0;
            margin: 0 6px 0 15px;
        }
    </style>
</head>

<body>
    <div class="box">
        <img src="../image/MI11.jpg" alt="">
        <p class="review">屏幕简直无敌！外观做工整体不错，雷宝宝给力！</p>
        <div class="appraise">来自于 11265634 的评价</div>
        <div class="info">
            <h4><a href="#">小米11 骁龙888 2K...</a></h4>
            <em>|</em>
            <span>3999元</span>
        </div>
    </div>
</body>

</html>
```

```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>综合案例-快报模板</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }

        li {
            list-style: none;
        }

        .box {
            width: 248px;
            height: 163px;
            border: 1px solid #ccc;
            margin: 100px auto;
        }

        .box h3 {
            height: 32px;
            border-bottom: 1px dotted #ccc;
            font-size: 14px;
            font-weight: 400;
            line-height: 32px;
            padding-left: 15px;
        }

        .box ul li a {
            font-size: 12px;
            color: #666;
            text-decoration: none;
        }

        .box ul li a:hover {
            text-decoration: underline;
        }

        .box ul li {
            height: 23px;
            line-height: 23px;
            padding-left: 20px;
        }

        .box ul {
            margin-top: 7px;
        }
    </style>
</head>

<body>
    <div class="box">
        <h3>品优购快报</h3>
        <ul>
            <li><a href="#">【特惠】爆款耳机5折秒！</a></li>
            <li><a href="#">【特惠】母亲节，健康好礼低至5折！</a></li>
            <li><a href="#">【特惠】语音折叠台灯99元！</a></li>
            <li><a href="#">【特惠】9.9元3D打印！</a></li>
            <li><a href="#">【特惠】格力智能空调立省1000元！</a></li>
        </ul>
    </div>
</body>

</html>
```



## 11、Pink 老师总结

### a、布局为啥用不同盒子,我只想用 div？

标签都是有语义的, 合理的地方用合理的标签。比如产品标题 就用 `h`, 大量文字段落就用 `p`

### b、为啥用辣么多类名？

类名就是给每个盒子起了一个名字,可以更好的找到这个盒子, 选取盒子更容易,后期维护也方便

### c、到底用 margin 还是 padding？

大部分情况两个可以混用，两者各有优缺点，但是根据实际情况，总是有更简单的方法实现

### d、自己做没有思路？

布局有很多种实现方式，同学们可以开始先模仿我的写法，然后再做出自己的风格

最后同学们一定多运用辅助工具,比如屏幕画笔，ps等等



> 原创思维导图，开源地址：https://github.com/JERRY-Z-J-R/JERRY-Mind

![](https://img-blog.csdnimg.cn/2021013115240524.png)




> **与我交流 >_^**
>
> **QQ：** 1846334075
>
> **WeChat：** zhoujirui54
>
> **个人网站：** <http://jerry-z-j-r.github.io>	
>
> **CSDN：** <https://blog.csdn.net/D_si_God>
>
> **Cnblogs：** <https://www.cnblogs.com/JERRY-Z-J-R/>
>
> **GitHub：** <https://github.com/JERRY-Z-J-R>
>
> **Gitee：** <https://gitee.com/JERRY-Z-J-R>
>
> **bilibili：** <https://space.bilibili.com/505277890>
>
> **微博：** <https://weibo.com/JERRY2454>
>
> **知乎：** <https://www.zhihu.com/people/JERRY-Z-J-R>