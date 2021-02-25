---
title: Pink老师 HTML CSS 学习笔记（第十七季）
date: 2021-02-20 22:29:09
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

# Pink老师 HTML CSS 学习笔记（第十七季）

# 【移动WEB开发之rem适配布局】

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Pink老师 HTML CSS 学习笔记（第十七季）](#pink%E8%80%81%E5%B8%88-html-css-%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%E7%AC%AC%E5%8D%81%E4%B8%83%E5%AD%A3)
- [【移动WEB开发之rem适配布局】](#%E7%A7%BB%E5%8A%A8web%E5%BC%80%E5%8F%91%E4%B9%8Brem%E9%80%82%E9%85%8D%E5%B8%83%E5%B1%80)
- [思考](#%E6%80%9D%E8%80%83)
- [一、rem 基础](#%E4%B8%80rem-%E5%9F%BA%E7%A1%80)
- [二、媒体查询](#%E4%BA%8C%E5%AA%92%E4%BD%93%E6%9F%A5%E8%AF%A2)
  - [2.1 什么是媒体查询](#21-%E4%BB%80%E4%B9%88%E6%98%AF%E5%AA%92%E4%BD%93%E6%9F%A5%E8%AF%A2)
  - [2.2 语法规范](#22-%E8%AF%AD%E6%B3%95%E8%A7%84%E8%8C%83)
  - [2.3 媒体查询+rem实现元素动态大小变化](#23-%E5%AA%92%E4%BD%93%E6%9F%A5%E8%AF%A2rem%E5%AE%9E%E7%8E%B0%E5%85%83%E7%B4%A0%E5%8A%A8%E6%80%81%E5%A4%A7%E5%B0%8F%E5%8F%98%E5%8C%96)
  - [2.4 引入资源（理解）](#24-%E5%BC%95%E5%85%A5%E8%B5%84%E6%BA%90%E7%90%86%E8%A7%A3)
- [三、Less 基础](#%E4%B8%89less-%E5%9F%BA%E7%A1%80)
  - [3.1 维护 css 的弊端](#31-%E7%BB%B4%E6%8A%A4-css-%E7%9A%84%E5%BC%8A%E7%AB%AF)
  - [3.2 Less 介绍](#32-less-%E4%BB%8B%E7%BB%8D)
  - [3.3 Less 安装（注意如果使用vscode无需安装less）](#33-less-%E5%AE%89%E8%A3%85%E6%B3%A8%E6%84%8F%E5%A6%82%E6%9E%9C%E4%BD%BF%E7%94%A8vscode%E6%97%A0%E9%9C%80%E5%AE%89%E8%A3%85less)
  - [3.4 Less 使用](#34-less-%E4%BD%BF%E7%94%A8)
  - [3.5 Less 变量](#35-less-%E5%8F%98%E9%87%8F)
  - [3.6 Less 编译](#36-less-%E7%BC%96%E8%AF%91)
  - [3.7 Less 嵌套](#37-less-%E5%B5%8C%E5%A5%97)
  - [3.8 Less 运算](#38-less-%E8%BF%90%E7%AE%97)
- [四、rem 适配方案](#%E5%9B%9Brem-%E9%80%82%E9%85%8D%E6%96%B9%E6%A1%88)
  - [思考](#%E6%80%9D%E8%80%83-1)
  - [答案](#%E7%AD%94%E6%A1%88)
  - [4.1 rem 实际开发适配方案](#41-rem-%E5%AE%9E%E9%99%85%E5%BC%80%E5%8F%91%E9%80%82%E9%85%8D%E6%96%B9%E6%A1%88)
  - [4.2 rem 适配方案技术使用（市场主流）](#42-rem-%E9%80%82%E9%85%8D%E6%96%B9%E6%A1%88%E6%8A%80%E6%9C%AF%E4%BD%BF%E7%94%A8%E5%B8%82%E5%9C%BA%E4%B8%BB%E6%B5%81)
  - [4.3 rem 实际开发适配方案1](#43-rem-%E5%AE%9E%E9%99%85%E5%BC%80%E5%8F%91%E9%80%82%E9%85%8D%E6%96%B9%E6%A1%881)
- [五、苏宁首页案例制作](#%E4%BA%94%E8%8B%8F%E5%AE%81%E9%A6%96%E9%A1%B5%E6%A1%88%E4%BE%8B%E5%88%B6%E4%BD%9C)
  - [5.1 技术选型](#51-%E6%8A%80%E6%9C%AF%E9%80%89%E5%9E%8B)
  - [5.2 搭建相关文件夹结构](#52-%E6%90%AD%E5%BB%BA%E7%9B%B8%E5%85%B3%E6%96%87%E4%BB%B6%E5%A4%B9%E7%BB%93%E6%9E%84)
  - [5.3 设置视口标签以及引入初始化样式](#53-%E8%AE%BE%E7%BD%AE%E8%A7%86%E5%8F%A3%E6%A0%87%E7%AD%BE%E4%BB%A5%E5%8F%8A%E5%BC%95%E5%85%A5%E5%88%9D%E5%A7%8B%E5%8C%96%E6%A0%B7%E5%BC%8F)
  - [5.4 设置公共 common.less 文件](#54-%E8%AE%BE%E7%BD%AE%E5%85%AC%E5%85%B1-commonless-%E6%96%87%E4%BB%B6)
  - [5.5 新建 index.less 文件](#55-%E6%96%B0%E5%BB%BA-indexless-%E6%96%87%E4%BB%B6)
  - [5.6 body 样式](#56-body-%E6%A0%B7%E5%BC%8F)
  - [5.7 案例结构及内容](#57-%E6%A1%88%E4%BE%8B%E7%BB%93%E6%9E%84%E5%8F%8A%E5%86%85%E5%AE%B9)
- [六、rem 适配方案2](#%E5%85%ADrem-%E9%80%82%E9%85%8D%E6%96%B9%E6%A1%882)
  - [6.1 简洁高效的 rem 适配方案 flexible.js](#61-%E7%AE%80%E6%B4%81%E9%AB%98%E6%95%88%E7%9A%84-rem-%E9%80%82%E9%85%8D%E6%96%B9%E6%A1%88-flexiblejs)
  - [6.2 使用适配方案2制作苏宁移动端首页](#62-%E4%BD%BF%E7%94%A8%E9%80%82%E9%85%8D%E6%96%B9%E6%A1%882%E5%88%B6%E4%BD%9C%E8%8B%8F%E5%AE%81%E7%A7%BB%E5%8A%A8%E7%AB%AF%E9%A6%96%E9%A1%B5)
  - [6.3 VSCode px 转换 rem 插件 cssrem](#63-vscode-px-%E8%BD%AC%E6%8D%A2-rem-%E6%8F%92%E4%BB%B6-cssrem)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


# 思考

- 方案 ？

1. 页面布局文字能否随着屏幕大小变化而变化？
2. 流式布局 和 `flex` 布局主要针对于宽度布局，那高度如何设置？
3. 怎么样让屏幕发生变化的时候元素高度和宽度等比例缩放？

# 一、rem 基础

**rem 单位**

`rem (root em)` 是一个相对单位，类似于 `em`，`em` 是父元素字体大小
不同的是 `rem` 的基准是相对于html元素的字体大小
比如，根元素（`html`）设置 `font-size=12px;` 非根元素设置 `width:2rem;` 则换成 `px` 表示就是 `24px`

```css
/* 根html 为 12px */
html {
	font-size: 12px;
}
/* 此时 div 的字体大小就是 24px */
div {
	font-size: 2rem;
}
```

`rem` 的优势：父元素文字大小可能不一致， 但是整个页面只有一个 `html`，可以很好来控制整个页面的元素大小

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>01-rem单位</title>
    <style>
        html {
            font-size: 12px;
        }

        div {
            font-size: 12px;
            width: 15rem;
            height: 15rem;
            background-color: purple;
        }

        p {
            /* 1. em相对于父元素 的字体大小来说的 */
            /* width: 10em;
            height: 10em; */
            /* 2. rem 相对于 html元素 字体大小来说的 */
            width: 10rem;
            height: 10rem;
            background-color: pink;
            /* 3.rem的优点就是可以通过修改html里面的文字大小来改变页面中元素的大小可以整体控制 */
        }
    </style>
</head>

<body>
    <div>
        <p></p>
    </div>

</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210221154055967.png)

![](https://img-blog.csdnimg.cn/2021022115405693.png)

# 二、媒体查询

## 2.1 什么是媒体查询

**媒体查询（`Media Query`）是 CSS3 新语法**

- 使用 `@media` 查询，可以针对不同的媒体类型定义不同的样式
- `@media` 可以针对不同的屏幕尺寸设置不同的样式
- 当你重置浏览器大小的过程中，页面也会根据浏览器的宽度和高度重新渲染页面
- 目前针对很多 苹果手机、Android 手机，平板等设备都用得到多媒体查询

![](https://img-blog.csdnimg.cn/20210221002600616.png)

## 2.2 语法规范

```css
@media mediatype and|not|only (media feature) {
	CSS-Code;
}
```

- 用 `@media` 开头 注意 `@` 符号
- `mediatype` 媒体类型
- 关键字 `and not only`
- `media feature` 媒体特性 必须有小括号包含

**1、mediatype 查询类型**

将不同的终端设备划分成不同的类型，称为媒体类型

![](https://img-blog.csdnimg.cn/20210221002949212.png)

**2、关键字**

关键字将媒体类型或多个媒体特性连接到一起做为媒体查询的条件

- `and`：可以将多个媒体特性连接到一起，相当于 “且” 的意思
- `not`：排除某个媒体类型，相当于 “非” 的意思，可以省略
- `only`：指定某个特定的媒体类型，可以省略

**3、媒体特性**

每种媒体类型都具体各自不同的特性，根据不同媒体类型的媒体特性设置不同的展示风格。我们暂且了解三个
注意他们要加小括号包含

![](https://img-blog.csdnimg.cn/20210221003325852.png)

**案例：根据页面宽度改变背景变色**

![](https://img-blog.csdnimg.cn/20210221003537515.png)

- 实现思路

1、按照 `从大到小` 的或者 `从小到大` 的思路

2、注意我们有 最大值 `max-width` 和 最小值 `min-width` 都是包含等于的

3、当屏幕 小于 `540像素`， 背景颜色变为 蓝色 （ `x <= 539`）

4、当屏幕 大于等于 `540像素` 并且 小于等于 `969像素` 的时候 背景颜色为 `绿色` ( `540 =< x <= 969`）

5、当屏幕 大于等于 `970像素` 的时候，背景颜色为 红色 （ `x >= 970`）

**注意：**为了防止混乱，媒体查询我们要按照 `从小到大` 或者 `从大到小` 的顺序来写，但是我们最喜欢的还是 `从小到大` 来写，这样代码更简洁

- 媒体查询从小到大优势代码分析

![](https://img-blog.csdnimg.cn/20210221004055777.png)

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>02-媒体查询</title>
    <style>
        /* 这句话的意思就是： 在我们屏幕上 并且 最大的宽度是 800像素 设置我们想要的样式 */
        /* max-width 小于等于800 */
        /* 媒体查询可以根据不同的屏幕尺寸在改变不同的样式 */

        @media screen and (max-width: 800px) {
            body {
                background-color: pink;
            }
        }

        @media screen and (max-width: 500px) {
            body {
                background-color: purple;
            }
        }
    </style>
</head>

<body>

</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210221154339618.png)

![](https://img-blog.csdnimg.cn/20210221154339753.png)

---

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>03-媒体查询案例修改背景颜色</title>
    <style>
        /* 1. 媒体查询一般按照从大到小或者 从小到大的顺序来 */
        /* 2. 小于540px 页面的背景颜色变为蓝色 */

        @media screen and (max-width: 539px) {
            body {
                background-color: blue;
            }
        }

        /* 3. 540 ~ 970 我们的页面颜色改为 绿色 */
        /* @media screen and (min-width: 540px) and (max-width: 969px) {
            body {
                background-color: green;
            }
        } */

        @media screen and (min-width: 540px) {
            body {
                background-color: green;
            }
        }

        /* 4. 大于等于970 我们页面的颜色改为 红色 */

        @media screen and (min-width: 970px) {
            body {
                background-color: red;
            }
        }

        /* 5. screen 还有 and 必须带上不能省略的 */
        /* 6. 我们的数字后面必须跟单位  970px   这个 px 不能省略的 */
    </style>
</head>

<body>

</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210221154511584.png)

![](https://img-blog.csdnimg.cn/20210221154511714.png)

## 2.3 媒体查询+rem实现元素动态大小变化

`rem` 单位是跟着 html 来走的，有了 `rem` 页面元素可以设置不同大小尺寸
媒体查询可以根据不同设备宽度来修改样式
媒体查询+rem 就可以实现不同设备宽度，实现页面元素大小的动态变化

**案例：媒体查询+rem实现元素变化**

![](https://img-blog.csdnimg.cn/20210221004251423.png)

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>04-媒体查询+rem实现元素动态变化</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }

        /* html {
            font-size: 100px;
        } */
        /* 从小到大的顺序 */

        @media screen and (min-width: 320px) {
            html {
                font-size: 50px;
            }
        }

        @media screen and (min-width: 640px) {
            html {
                font-size: 100px;
            }
        }

        .top {
            height: 1rem;
            font-size: .5rem;
            background-color: green;
            color: #fff;
            text-align: center;
            line-height: 1rem;
        }
    </style>
</head>

<body>
    <div class="top">购物车</div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/2021022115465192.png)

![](https://img-blog.csdnimg.cn/20210221154651267.png)

## 2.4 引入资源（理解）

当样式比较繁多的时候，我们可以针对不同的媒体使用不同 `stylesheets`（样式表）
原理，就是直接在 `link` 中判断设备的尺寸，然后引用不同的 `css` 文件

- 1、语法规范

```html
<link rel="stylesheet" media="mediatype and|not|only (media feature)" href="mystylesheet.css">
```

- 2、示例

```html
<link rel="stylesheet" href="styleA.css" media="screen and (min-width: 400px)">
```

案例：

- style320.css

```css
div {
  width: 100%;
  height: 100px;
}

div:nth-child(1) {
  background-color: pink;
}

div:nth-child(2) {
  background-color: purple;
}
```

- style640.css

```css
div {
  float: left;
  width: 50%;
  height: 100px;
}

div:nth-child(1) {
  background-color: pink;
}

div:nth-child(2) {
  background-color: purple;
}
```

- 05-引入资源.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>05-引入资源</title>
    <style>
        /* 当我们屏幕大于等于 640px以上的，我们让div 一行显示2个 */
        /* 当我们屏幕小于640 我们让div一行显示一个 */
        /* 一个建议： 我们媒体查询最好的方法是从小到大 */
        /* 引入资源就是 针对于不同的屏幕尺寸 调用不同的css文件 */
    </style>
    <link rel="stylesheet" href="style320.css" media="screen and (min-width: 320px)">
    <link rel="stylesheet" href="style640.css" media="screen and (min-width: 640px)">
</head>

<body>
    <div>1</div>
    <div>2</div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210221154805832.png)

![](https://img-blog.csdnimg.cn/20210221154806182.png)

# 三、Less 基础

## 3.1 维护 css 的弊端

CSS 是一门非程序式语言，没有变量、函数、SCOPE（作用域）等概念

- CSS 需要书写大量看似没有逻辑的代码，CSS 冗余度是比较高的
- 不方便维护及扩展，不利于复用
- CSS 没有很好的计算能力
- 非前端开发工程师来讲，往往会因为缺少 CSS 编写经验而很难写出组织良好且易于维护的 CSS 代码项目

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>06-CSS的缺点</title>
    <style>
        html {
            font-size: 50px;
        }

        img {
            /* width: 82px;
            height: 82px; */
            /* width: 1.64rem;
            height: 1.64rem; */
            /* width: 82 / 50; */
        }

        div {
            background-color: pink;
        }

        p {
            background-color: pink;
        }

        span {
            background-color: pink;
        }
    </style>
</head>

<body>

</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210221155010378.png)

![](https://img-blog.csdnimg.cn/20210221155010448.png)

## 3.2 Less 介绍

`Less`（`Leaner Style Sheets` 的缩写） 是一门 CSS 扩展语言，也成为CSS预处理器
做为 CSS 的一种形式的扩展，它并没有减少 CSS 的功能，而是在现有的 CSS 语法上，为CSS加入程序式语言的特性
它在 CSS 的语法基础之上，引入了变量，`Mixin`（混入），运算以及函数等功能，大大简化了 CSS 的编写，并且降低了 CSS 的维护成本，就像它的名称所说的那样，`Less` 可以让我们用更少的代码做更多的事情
`Less` 中文网址： [http://lesscss.cn/](http://lesscss.cn/)
常见的 CSS 预处理器：`Sass`、`Less`、`Stylus`
一句话：`Less` 是一门 CSS 预处理语言，它扩展了 CSS 的动态特性

## 3.3 Less 安装（注意如果使用vscode无需安装less）

- 1、安装nodejs，可选择版本(8.0)，网址：[http://nodejs.cn/download/](http://nodejs.cn/download/)
- 2、检查是否安装成功，使用 `cmd命令`（win10 是 Window + R 打开 运行输入 `cmd`） --- 输入“ `node –v` ” 查看版本即可
- 基于 `nodejs` 在线安装 `Less`，使用cmd命令 “ `npm install -g less` ” 即可
- 检查是否安装成功，使用 `cmd命令` “ `lessc -v` ” 查看版本即可

![](https://img-blog.csdnimg.cn/20210221005218731.png)

## 3.4 Less 使用

我们首先新建一个后缀名为 `.less` 的文件， 在这个 `less` 文件里面书写 `less` 语句

- Less 变量
- Less 编译
- Less 嵌套
- Less 运算

案例：

- my.less

```less
// 定义一个粉色的变量
@color: pink;
// 错误的变量名  @1color   @color~@#
// 变量名区分大小写  @color  和  @Color 是两个不同的变量
// 定义了一个 字体为14像素的变量
@font14: 14px;
body {
  background-color: @color;
}

div {
  color: @color;
  font-size: @font14;
}

a {
  font-size: @font14;
}
```

- my.css

```css
body {
  background-color: pink;
}

div {
  color: pink;
  font-size: 14px;
}

a {
  font-size: 14px;
}
```

- 07-less的使用.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>07-less的使用</title>
    <link rel="stylesheet" href="my.css">
</head>

<body>
    <div>
        我的颜色也是粉色
    </div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210221155153579.png)

![](https://img-blog.csdnimg.cn/20210221155153778.png)

## 3.5 Less 变量

变量是指没有固定的值，可以改变的。因为我们 CSS 中的一些颜色和数值等经常使用

`@变量名:值;`

**1、变量命名规范**

- 必须有@为前缀
- 不能包含特殊字符
- 不能以数字开头
- 大小写敏感

`@color: pink;`

**2、变量使用规范**

```less
//直接使用
body {
	color:@color;
}
a:hover {
	color:@color;
}
```

## 3.6 Less 编译

本质上，Less 包含一套自定义的语法及一个解析器，用户根据这些语法定义自己的样式规则，这些规则最终会通过解析器，编译生成对应的 CSS 文件
所以，我们需要把我们的 less 文件，编译生成为 css 文件，这样我们的 html 页面才能使用

- VSCode Less 插件

`Easy LESS` 插件用来把 `less` 文件编译为 `css` 文件
安装完毕插件，重新加载下 `VSCode`
只要保存一下 `Less` 文件，会自动生成 `CSS` 文件

![](https://img-blog.csdnimg.cn/20210221010234130.png)

## 3.7 Less 嵌套

我们经常用到选择器的嵌套

```less
#header .logo {
	width: 300px;
}
```

Less 嵌套写法

```less
#header {
	.logo {
		width: 300px;
	}
}
```

如果遇见 （ `交集` | `伪类` | `伪元素选择器` ）

- 内层选择器的前面没有 `&` 符号，则它被解析为父选择器的后代
- 如果有 `&` 符号，它就被解析为父元素自身或父元素的伪类

```less
a:hover {
	color:red;
}
```

Less 嵌套写法

```less
a{
	&:hover{
		color:red;
	}
}
```

案例：

- nest.less

```less
.header {
  width: 200px;
  height: 200px;
  background-color: pink;
  // 1. less嵌套 子元素的样式直接写到父元素里面就好了
  a {
    color: red;
    // 2. 如果有伪类、交集选择器、 伪元素选择器 我们内层选择器的前面需要加&
    &:hover {
      color: blue;
    }
  }
}

.nav {
  .logo {
    color: green;
  }
  &::before {
    content: "";
  }
}
```

- nest.css

```css
.header {
  width: 200px;
  height: 200px;
  background-color: pink;
}

.header a {
  color: red;
}

.header a:hover {
  color: blue;
}

.nav .logo {
  color: green;
}

.nav::before {
  content: "";
}
```

- 08-less嵌套.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>08-less嵌套</title>
    <style>
        /* .header {}
        .header a {} */
    </style>
    <link rel="stylesheet" href="nest.css">
</head>

<body>
    <div class="header">
        <a href="#">文字</a>
    </div>
    <div class="nav">
        <div class="logo">传智播客</div>
    </div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210221155858362.png)

![](https://img-blog.csdnimg.cn/20210221155858425.png)

## 3.8 Less 运算

任何数字、颜色或者变量都可以参与运算，就是 Less 提供了加（+）、减（-）、乘（*）、除（/）算术运算

```less
/*Less 里面写*/
@witdh: 10px + 5;
div {
	border: @witdh solid red;
}
/*生成的css*/
div {
	border: 15px solid red;
}
/*Less 甚至还可以这样 */
width: (@width + 5) * 2;
```

**注意：**

- 乘号（`*`）和除号（`/`）的写法
- 运算符中间左右有个空格隔开 `1px + 5`
- 对于两个不同的单位的值之间的运算，运算结果的值取第一个值的单位
- 如果两个值之间只有一个值有单位，则运算结果就取该单位

案例：

- count.less

```less
@baseFont: 50px;
html {
  font-size: @baseFont;
}

@border: 5px + 5;
div {
  width: 200px - 50;
  height: (200px + 50px) * 2;
  border: @border solid red;
  background-color: #666 - #222;
}

img {
  width: 82rem / @baseFont;
  height: 82rem / @baseFont;
}
// 1. 我们运算符的左右两侧必须敲一个空格隔开
// 2. 两个数参与运算  如果只有一个数有单位，则最后的结果就以这个单位为准
// 3. 两个数参与运算，如果2个数都有单位，而且不一样的单位 最后的结果以第一个单位为准
```

- count.css

```css
html {
  font-size: 50px;
}

div {
  width: 150px;
  height: 500px;
  border: 10px solid red;
  background-color: #444444;
}

img {
  width: 82rem / 50px;
  height: 82rem / 50px;
}
```

- 09-less运算.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>09-less运算</title>
    <link rel="stylesheet" href="count.css">
</head>

<body>
    <div></div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210221160135429.png)

![](https://img-blog.csdnimg.cn/20210221160135629.png)

# 四、rem 适配方案

## 思考

- rem 适配方案

1、我们适配的目标是什么？

2、怎么去达到这个目标的？

3、在实际的开发当中使用？

## 答案

- rem 适配方案

1、让一些不能等比自适应的元素，达到当设备尺寸发生改变的时候，等比例适配当前设备

2、使用媒体查询根据不同设备按比例设置 html 的字体大小，然后页面元素使用 `rem` 做尺寸单位，当 `html` 字体大小变化元素尺寸也会发生变化，从而达到等比缩放的适配

## 4.1 rem 实际开发适配方案

1、按照设计稿与设备宽度的比例，动态计算并设置 html 根标签的 `font-size` 大小；（媒体查询）

2、CSS 中，设计稿元素的宽、高、相对位置等取值，按照同等比例换算为 `rem` 为单位的值

![](https://img-blog.csdnimg.cn/20210221011233477.png)

## 4.2 rem 适配方案技术使用（市场主流）

![](https://img-blog.csdnimg.cn/20210221011355599.png)

**总结：**

1、两种方案现在都存在

2、方案2 更简单，现阶段大家无需了解里面的 `js` 代码

## 4.3 rem 实际开发适配方案1

rem + 媒体查询 + less 技术

- 1、设计稿常见尺寸宽度

![](https://img-blog.csdnimg.cn/2021022101205389.png)

一般情况下，我们以一套或两套效果图适应大部分的屏幕，放弃极端屏或对其优雅降级，牺牲一些效果，现在基本以 750 为准

- 2、动态设置 html 标签 font-size 大小

1、假设设计稿是 `750px`
2、假设我们把整个屏幕划分为 15 等份（划分标准不一可以是 20 份也可以是 10 等份）
3、每一份作为 html 字体大小，这里就是 `50px`
4、那么在 `320px` 设备的时候，字体大小为 `320/15` 就是 `21.33px`
5、用我们页面元素的大小 除以不同的 html 字体大小会发现他们比例还是相同的
6、比如我们以 `750` 为标准设计稿
7、一个 `100 * 100` 像素的页面元素在 `750` 屏幕下， 就是 `100 / 50` 转换为 `rem` 是 `2rem * 2 rem` 比例是 `1比1`
8、`320` 屏幕下， html 字体大小为 `21.33` 则 `2rem = 42.66px` 此时宽和高都是 `42.66` 但是 宽和高的比例还是 `1比1`
9、但是已经能实现不同屏幕下 页面元素盒子等比例缩放的效果

- 3、元素大小取值方法

1、最后的公式：`页面元素的 rem值` = `页面元素值（px）` / （ `屏幕宽度` / `划分的份数` ）
2、屏幕宽度 / 划分的份数 就是 html `font-size` 的大小
3、或者：`页面元素的 rem值` = `页面元素值（px）` / `html font-size 字体大小`

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>10-rem适配方案</title>
    <style>
        @media screen and (min-width: 320px) {
            html {
                font-size: 21.33px;
            }
        }

        @media screen and (min-width: 750px) {
            html {
                font-size: 50px;
            }
        }

        div {
            width: 2rem;
            height: 2rem;
            background-color: pink;
        }

        /* 1. 首先我们选一套标准尺寸 750为准 
           2. 我们用屏幕尺寸 除以 我们划分的份数 得到了 html 里面的文字大小 但是我们知道不同屏幕下得到的文字大小是不一样的
           3. 页面元素的rem值 =  页面元素在 750像素的下px值 / html 里面的文字大小 */
    </style>
</head>

<body>
    <div></div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/202102211608155.png)

![](https://img-blog.csdnimg.cn/2021022116081579.png)

# 五、苏宁首页案例制作

- 访问地址：[m.suning.com](m.suning.com)

![](https://img-blog.csdnimg.cn/20210221012236684.png)

## 5.1 技术选型

- 方案：我们采取单独制作移动页面方案
- 技术：布局采取 rem 适配布局（less + rem + 媒体查询）
- 设计图： 本设计图采用 750px 设计尺寸

## 5.2 搭建相关文件夹结构

![](https://img-blog.csdnimg.cn/20210221012520267.png)

## 5.3 设置视口标签以及引入初始化样式

```html
<meta name="viewport" content="width=device-width, user-scalable=no,
initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
<link rel="stylesheet" href="css/normalize.css">
```

## 5.4 设置公共 common.less 文件

1. 新建 `common.less` 设置好最常见的屏幕尺寸，利用媒体查询设置不同的 html 字体大小，因为除了首页其他页面也需要
2. 我们关心的尺寸有 320px、360px、375px、384px、400px、414px、424px、480px、540px、720px、750px
3. 划分的份数我们定为 15等份
4. 因为我们 pc端 也可以打开我们苏宁移动端首页，我们默认 html 字体大小为 50px，注意这句话写到最上面

## 5.5 新建 index.less 文件

1. 新建 `index.less` 这里面写首页的样式

2. 将刚才设置好的 `common.less` 引入到 `index.less` 里面 语法如下：

```less
  // 在 index.less 中导入 common.less 文件
  @import “common”
```

3. 生成 `index.css` 引入到 `index.html` 里面

## 5.6 body 样式

```css
body {
	min-width: 320px;
	width: 15rem;
	margin: 0 auto;
	line-height: 1.5;
	font-family: Arial, Helvetica;
	background: #F2F2F2;
}
```

## 5.7 案例结构及内容

![](https://img-blog.csdnimg.cn/20210221161151126.png)

![](https://img-blog.csdnimg.cn/20210221161151161.png)

![](https://img-blog.csdnimg.cn/20210221161151148.png)

![](https://img-blog.csdnimg.cn/20210221161151206.png)

- common.less

```less
// 设置常见的屏幕尺寸 修改里面的html文字大小
a {
    text-decoration: none;
}

// 一定要写到最上面
html {
    font-size: 50px;
}

// 我们此次定义的划分的份数 为 15
@no: 15;
// 320
@media screen and (min-width: 320px) {
    html {
        font-size: 320px / @no;
    }
}

// 360
@media screen and (min-width: 360px) {
    html {
        font-size: 360px / @no;
    }
}

// 375 iphone 678
@media screen and (min-width: 375px) {
    html {
        font-size: 375px / @no;
    }
}

// 384
@media screen and (min-width: 384px) {
    html {
        font-size: 384px / @no;
    }
}

// 400
@media screen and (min-width: 400px) {
    html {
        font-size: 400px / @no;
    }
}

// 414
@media screen and (min-width: 414px) {
    html {
        font-size: 414px / @no;
    }
}

// 424
@media screen and (min-width: 424px) {
    html {
        font-size: 424px / @no;
    }
}

// 480
@media screen and (min-width: 480px) {
    html {
        font-size: 480px / @no;
    }
}

// 540
@media screen and (min-width: 540px) {
    html {
        font-size: 540px / @no;
    }
}

// 720
@media screen and (min-width: 720px) {
    html {
        font-size: 720px / @no;
    }
}

// 750
@media screen and (min-width: 750px) {
    html {
        font-size: 750px / @no;
    }
}
```

- common.css

```css
a {
  text-decoration: none;
}

html {
  font-size: 50px;
}

@media screen and (min-width: 320px) {
  html {
    font-size: 320px / 15;
  }
}

@media screen and (min-width: 360px) {
  html {
    font-size: 360px / 15;
  }
}

@media screen and (min-width: 375px) {
  html {
    font-size: 375px / 15;
  }
}

@media screen and (min-width: 384px) {
  html {
    font-size: 384px / 15;
  }
}

@media screen and (min-width: 400px) {
  html {
    font-size: 400px / 15;
  }
}

@media screen and (min-width: 414px) {
  html {
    font-size: 414px / 15;
  }
}

@media screen and (min-width: 424px) {
  html {
    font-size: 424px / 15;
  }
}

@media screen and (min-width: 480px) {
  html {
    font-size: 480px / 15;
  }
}

@media screen and (min-width: 540px) {
  html {
    font-size: 540px / 15;
  }
}

@media screen and (min-width: 720px) {
  html {
    font-size: 720px / 15;
  }
}

@media screen and (min-width: 750px) {
  html {
    font-size: 750px / 15;
  }
}
```

- index.less

```less
// 首页的样式less文件
@import "common";
// @import 导入的意思 可以把一个样式文件导入到另外一个样式文件里面
// link 是把一个 样式文件引入到 html页面里面
body {
    min-width: 320px;
    width: 15rem;
    margin: 0 auto;
    line-height: 1.5;
    font-family: Arial,Helvetica;
    background: #F2F2F2;
}

// 页面元素rem计算公式： 页面元素的px / html 字体大小 50
// search-content
@baseFont: 50;
.search-content {
    display: flex;
    position: fixed;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 15rem;
    height: 88rem / @baseFont;
    background-color:#FFC001;
    .classify {
        width: 44rem / @baseFont;
        height: 70rem / @baseFont;
        margin: 11rem / @baseFont 25rem / @baseFont 7rem / @baseFont 24rem / @baseFont;
        background: url(../images/classify.png) no-repeat;
        // 背景缩放
        background-size: 44rem / @baseFont 70rem / @baseFont;
    }
    .search {
        flex: 1;
        input {
            outline: none;
            width: 100%;
            border: 0;
            height: 66rem / @baseFont;
            border-radius: 33rem / @baseFont;
            background-color:#FFF2CC;
            margin-top: 12rem / @baseFont;
            font-size: 25rem / @baseFont;
            padding-left: 55rem / @baseFont;
            color: #757575;
        }
    }
    .login {
        width: 75rem / @baseFont;
        height: 70rem / @baseFont;
        line-height: 70rem / @baseFont;
        margin: 10rem / @baseFont;
        font-size: 25rem / @baseFont;
        text-align: center;
        color: #fff;

    }
}

// banner
.banner {
    width: 750rem / @baseFont;
    height: 368rem / @baseFont;
    img {
        width: 100%;
        height: 100%;
    }
}

// ad
.ad {
    display: flex;
    a {
        flex: 1;
        img {
            width: 100%;
        }
    }
}

// nav
nav {
    width: 750rem / @baseFont;
    a {
        float: left;
        width: 150rem / @baseFont;
        height: 140rem / @baseFont;
        text-align: center;
        img {
            display: block;
            width: 82rem / @baseFont;
            height: 82rem / @baseFont;
            margin: 10rem / @baseFont auto 0;
        }
        span {
            font-size: 25rem / @baseFont;
            color: #333;
        }
    }
}
```

- index.css

```css
a {
  text-decoration: none;
}

html {
  font-size: 50px;
}

@media screen and (min-width: 320px) {
  html {
    font-size: 21.33333333px;
  }
}

@media screen and (min-width: 360px) {
  html {
    font-size: 24px;
  }
}

@media screen and (min-width: 375px) {
  html {
    font-size: 25px;
  }
}

@media screen and (min-width: 384px) {
  html {
    font-size: 25.6px;
  }
}

@media screen and (min-width: 400px) {
  html {
    font-size: 26.66666667px;
  }
}

@media screen and (min-width: 414px) {
  html {
    font-size: 27.6px;
  }
}

@media screen and (min-width: 424px) {
  html {
    font-size: 28.26666667px;
  }
}

@media screen and (min-width: 480px) {
  html {
    font-size: 32px;
  }
}

@media screen and (min-width: 540px) {
  html {
    font-size: 36px;
  }
}

@media screen and (min-width: 720px) {
  html {
    font-size: 48px;
  }
}

@media screen and (min-width: 750px) {
  html {
    font-size: 50px;
  }
}

body {
  min-width: 320px;
  width: 15rem;
  margin: 0 auto;
  line-height:  1.5;
  font-family:  Arial,Helvetica;
  background:  #F2F2F2;
}

.search-content {
  display: flex;
  position: fixed;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 15rem;
  height: 1.76rem;
  background-color: #FFC001;
}

.search-content .classify {
  width: 0.88rem;
  height: 1.4rem;
  margin: 0.22rem 0.5rem 0.14rem 0.48rem;
  background: url(../images/classify.png) no-repeat;
  background-size: 0.88rem 1.4rem;
}

.search-content .search {
  flex: 1;
}

.search-content .search input {
  outline: none;
  width: 100%;
  border: 0;
  height: 1.32rem;
  border-radius: 0.66rem;
  background-color: #FFF2CC;
  margin-top: 0.24rem;
  font-size: 0.5rem;
  padding-left: 1.1rem;
  color: #757575;
}

.search-content .login {
  width: 1.5rem;
  height: 1.4rem;
  line-height: 1.4rem;
  margin: 0.2rem;
  font-size: 0.5rem;
  text-align: center;
  color: #fff;
}

.banner {
  width: 15rem;
  height: 7.36rem;
}

.banner img {
  width: 100%;
  height: 100%;
}

.ad {
  display: flex;
}

.ad a {
  flex: 1;
}

.ad a img {
  width: 100%;
}

nav {
  width: 15rem;
}

nav a {
  float: left;
  width: 3rem;
  height: 2.8rem;
  text-align: center;
}

nav a img {
  display: block;
  width: 1.64rem;
  height: 1.64rem;
  margin: 0.2rem auto 0;
}

nav a span {
  font-size: 0.5rem;
  color: #333;
}
```

- normalize.css

```css
/*! normalize.css v5.0.0 | MIT License | github.com/necolas/normalize.css */

/**
 * 1. Change the default font family in all browsers (opinionated).
 * 2. Correct the line height in all browsers.
 * 3. Prevent adjustments of font size after orientation changes in
 *    IE on Windows Phone and in iOS.
 */

/* Document
   ========================================================================== */

html {
  font-family: sans-serif; /* 1 */
  line-height: 1.15; /* 2 */
  -ms-text-size-adjust: 100%; /* 3 */
  -webkit-text-size-adjust: 100%; /* 3 */
}

/* Sections
   ========================================================================== */

/**
 * Remove the margin in all browsers (opinionated).
 */

body {
  margin: 0;
}

/**
 * Add the correct display in IE 9-.
 */

article,
aside,
footer,
header,
nav,
section {
  display: block;
}

/**
 * Correct the font size and margin on `h1` elements within `section` and
 * `article` contexts in Chrome, Firefox, and Safari.
 */

h1 {
  font-size: 2em;
  margin: 0.67em 0;
}

/* Grouping content
   ========================================================================== */

/**
 * Add the correct display in IE 9-.
 * 1. Add the correct display in IE.
 */

figcaption,
figure,
main { /* 1 */
  display: block;
}

/**
 * Add the correct margin in IE 8.
 */

figure {
  margin: 1em 40px;
}

/**
 * 1. Add the correct box sizing in Firefox.
 * 2. Show the overflow in Edge and IE.
 */

hr {
  box-sizing: content-box; /* 1 */
  height: 0; /* 1 */
  overflow: visible; /* 2 */
}

/**
 * 1. Correct the inheritance and scaling of font size in all browsers.
 * 2. Correct the odd `em` font sizing in all browsers.
 */

pre {
  font-family: monospace, monospace; /* 1 */
  font-size: 1em; /* 2 */
}

/* Text-level semantics
   ========================================================================== */

/**
 * 1. Remove the gray background on active links in IE 10.
 * 2. Remove gaps in links underline in iOS 8+ and Safari 8+.
 */

a {
  background-color: transparent; /* 1 */
  -webkit-text-decoration-skip: objects; /* 2 */
}

/**
 * Remove the outline on focused links when they are also active or hovered
 * in all browsers (opinionated).
 */

a:active,
a:hover {
  outline-width: 0;
}

/**
 * 1. Remove the bottom border in Firefox 39-.
 * 2. Add the correct text decoration in Chrome, Edge, IE, Opera, and Safari.
 */

abbr[title] {
  border-bottom: none; /* 1 */
  text-decoration: underline; /* 2 */
  text-decoration: underline dotted; /* 2 */
}

/**
 * Prevent the duplicate application of `bolder` by the next rule in Safari 6.
 */

b,
strong {
  font-weight: inherit;
}

/**
 * Add the correct font weight in Chrome, Edge, and Safari.
 */

b,
strong {
  font-weight: bolder;
}

/**
 * 1. Correct the inheritance and scaling of font size in all browsers.
 * 2. Correct the odd `em` font sizing in all browsers.
 */

code,
kbd,
samp {
  font-family: monospace, monospace; /* 1 */
  font-size: 1em; /* 2 */
}

/**
 * Add the correct font style in Android 4.3-.
 */

dfn {
  font-style: italic;
}

/**
 * Add the correct background and color in IE 9-.
 */

mark {
  background-color: #ff0;
  color: #000;
}

/**
 * Add the correct font size in all browsers.
 */

small {
  font-size: 80%;
}

/**
 * Prevent `sub` and `sup` elements from affecting the line height in
 * all browsers.
 */

sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}

sub {
  bottom: -0.25em;
}

sup {
  top: -0.5em;
}

/* Embedded content
   ========================================================================== */

/**
 * Add the correct display in IE 9-.
 */

audio,
video {
  display: inline-block;
}

/**
 * Add the correct display in iOS 4-7.
 */

audio:not([controls]) {
  display: none;
  height: 0;
}

/**
 * Remove the border on images inside links in IE 10-.
 */

img {
  border-style: none;
}

/**
 * Hide the overflow in IE.
 */

svg:not(:root) {
  overflow: hidden;
}

/* Forms
   ========================================================================== */

/**
 * 1. Change the font styles in all browsers (opinionated).
 * 2. Remove the margin in Firefox and Safari.
 */

button,
input,
optgroup,
select,
textarea {
  font-family: sans-serif; /* 1 */
  font-size: 100%; /* 1 */
  line-height: 1.15; /* 1 */
  margin: 0; /* 2 */
}

/**
 * Show the overflow in IE.
 * 1. Show the overflow in Edge.
 */

button,
input { /* 1 */
  overflow: visible;
}

/**
 * Remove the inheritance of text transform in Edge, Firefox, and IE.
 * 1. Remove the inheritance of text transform in Firefox.
 */

button,
select { /* 1 */
  text-transform: none;
}

/**
 * 1. Prevent a WebKit bug where (2) destroys native `audio` and `video`
 *    controls in Android 4.
 * 2. Correct the inability to style clickable types in iOS and Safari.
 */

button,
html [type="button"], /* 1 */
[type="reset"],
[type="submit"] {
  -webkit-appearance: button; /* 2 */
}

/**
 * Remove the inner border and padding in Firefox.
 */

button::-moz-focus-inner,
[type="button"]::-moz-focus-inner,
[type="reset"]::-moz-focus-inner,
[type="submit"]::-moz-focus-inner {
  border-style: none;
  padding: 0;
}

/**
 * Restore the focus styles unset by the previous rule.
 */

button:-moz-focusring,
[type="button"]:-moz-focusring,
[type="reset"]:-moz-focusring,
[type="submit"]:-moz-focusring {
  outline: 1px dotted ButtonText;
}

/**
 * Change the border, margin, and padding in all browsers (opinionated).
 */

fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}

/**
 * 1. Correct the text wrapping in Edge and IE.
 * 2. Correct the color inheritance from `fieldset` elements in IE.
 * 3. Remove the padding so developers are not caught out when they zero out
 *    `fieldset` elements in all browsers.
 */

legend {
  box-sizing: border-box; /* 1 */
  color: inherit; /* 2 */
  display: table; /* 1 */
  max-width: 100%; /* 1 */
  padding: 0; /* 3 */
  white-space: normal; /* 1 */
}

/**
 * 1. Add the correct display in IE 9-.
 * 2. Add the correct vertical alignment in Chrome, Firefox, and Opera.
 */

progress {
  display: inline-block; /* 1 */
  vertical-align: baseline; /* 2 */
}

/**
 * Remove the default vertical scrollbar in IE.
 */

textarea {
  overflow: auto;
}

/**
 * 1. Add the correct box sizing in IE 10-.
 * 2. Remove the padding in IE 10-.
 */

[type="checkbox"],
[type="radio"] {
  box-sizing: border-box; /* 1 */
  padding: 0; /* 2 */
}

/**
 * Correct the cursor style of increment and decrement buttons in Chrome.
 */

[type="number"]::-webkit-inner-spin-button,
[type="number"]::-webkit-outer-spin-button {
  height: auto;
}

/**
 * 1. Correct the odd appearance in Chrome and Safari.
 * 2. Correct the outline style in Safari.
 */

[type="search"] {
  -webkit-appearance: textfield; /* 1 */
  outline-offset: -2px; /* 2 */
}

/**
 * Remove the inner padding and cancel buttons in Chrome and Safari on macOS.
 */

[type="search"]::-webkit-search-cancel-button,
[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}

/**
 * 1. Correct the inability to style clickable types in iOS and Safari.
 * 2. Change font properties to `inherit` in Safari.
 */

::-webkit-file-upload-button {
  -webkit-appearance: button; /* 1 */
  font: inherit; /* 2 */
}

/* Interactive
   ========================================================================== */

/*
 * Add the correct display in IE 9-.
 * 1. Add the correct display in Edge, IE, and Firefox.
 */

details, /* 1 */
menu {
  display: block;
}

/*
 * Add the correct display in all browsers.
 */

summary {
  display: list-item;
}

/* Scripting
   ========================================================================== */

/**
 * Add the correct display in IE 9-.
 */

canvas {
  display: inline-block;
}

/**
 * Add the correct display in IE.
 */

template {
  display: none;
}

/* Hidden
   ========================================================================== */

/**
 * Add the correct display in IE 10-.
 */

[hidden] {
  display: none;
}
```

- index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="css/normalize.css">
    <link rel="stylesheet" href="css/index.css">
    <title>Document</title>
</head>

<body>
    <!-- 顶部搜索框 -->
    <div class="search-content">
        <a href="#" class="classify"></a>
        <div class="search">
            <form action="">
                <input type="search" value="厨卫保暖季 哒哒哒">
            </form>
        </div>
        <a href="#" class="login">登录</a>
    </div>
    <!-- banner部分 -->
    <div class="banner">
        <img src="upload/banner.gif" alt="">
    </div>
    <!-- 广告部分 -->
    <div class="ad">
        <a href="#"><img src="upload/ad1.gif" alt=""></a>
        <a href="#"><img src="upload/ad2.gif" alt=""></a>
        <a href="#"><img src="upload/ad3.gif" alt=""></a>
    </div>
    <!-- nav模块 -->
    <nav>
        <a href="#">
            <img src="upload/nav1.png" alt="">
            <span>爆款手机</span>
        </a>
        <a href="#">
            <img src="upload/nav1.png" alt="">
            <span>爆款手机</span>
        </a>
        <a href="#">
            <img src="upload/nav1.png" alt="">
            <span>爆款手机</span>
        </a>
        <a href="#">
            <img src="upload/nav1.png" alt="">
            <span>爆款手机</span>
        </a>
        <a href="#">
            <img src="upload/nav1.png" alt="">
            <span>爆款手机</span>
        </a>
        <a href="#">
            <img src="upload/nav1.png" alt="">
            <span>爆款手机</span>
        </a>
        <a href="#">
            <img src="upload/nav1.png" alt="">
            <span>爆款手机</span>
        </a>
        <a href="#">
            <img src="upload/nav1.png" alt="">
            <span>爆款手机</span>
        </a>
        <a href="#">
            <img src="upload/nav1.png" alt="">
            <span>爆款手机</span>
        </a>
        <a href="#">
            <img src="upload/nav1.png" alt="">
            <span>爆款手机</span>
        </a>

    </nav>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210221162212899.png)

![](https://img-blog.csdnimg.cn/20210221162211952.png)

# 六、rem 适配方案2

## 6.1 简洁高效的 rem 适配方案 flexible.js

![](https://img-blog.csdnimg.cn/20210221013137116.png)

手机淘宝团队出的简洁高效 移动端适配库
我们再也不需要在写不同屏幕的媒体查询，因为里面 js 做了处理
它的原理是把当前设备划分为10等份，但是不同设备下，比例还是一致的
我们要做的，就是确定好我们当前设备的 html 文字大小就可以了
比如当前设计稿是 750px， 那么我们只需要把 html 文字大小设置为 75px(750px / 10) 就可以
里面页面元素 rem 值： 页面元素的 px 值 / 75
剩余的，让 flexible.js 来去算
github地址：[https://github.com/amfe/lib-flexible](https://github.com/amfe/lib-flexible)

## 6.2 使用适配方案2制作苏宁移动端首页

- 1、技术选型

方案：我们采取单独制作移动页面方案
技术：布局采取rem适配布局2（flexible.js + rem）
设计图： 本设计图采用 750px 设计尺寸

- 2、搭建相关文件夹结构

![](https://img-blog.csdnimg.cn/20210221013525730.png)

- 3、设置视口标签以及引入初始化样式还有 js 文件

```html
<meta name="viewport" content="width=device-width, user-scalable=no,
initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
<link rel="stylesheet" href="css/normalize.css">
<link rel="stylesheet" href="css/index.css">
```

我们页面需要引入 这个 js 文件

```html
在 index.html 中 引入 flexible.js 这个文件
<script src=“js/flexible.js”> </script>
```

- 4、body 样式

```css
body {
	min-width: 320px;
	width: 15rem;
	margin: 0 auto;
	line-height: 1.5;
	font-family: Arial,Helvetica;
	background: #F2F2F2;
}
```

- **案例结构及内容**

![](https://img-blog.csdnimg.cn/2021022116255819.png)

![](https://img-blog.csdnimg.cn/2021022116255826.png)

![](https://img-blog.csdnimg.cn/2021022116255822.png)

![](https://img-blog.csdnimg.cn/20210221162557858.png)

![](https://img-blog.csdnimg.cn/20210221162558379.png)

- index.css

```css
body {
  min-width: 320px;
  max-width: 750px;
  /* flexible 给我们划分了 10 等份 */
  width: 10rem;
  margin: 0 auto;
  line-height: 1.5;
  font-family: Arial, Helvetica;
  background: #f2f2f2;
}

a {
  text-decoration: none;
  font-size: 0.333333rem;
}

/* 这个插件默认的html文字大小 cssroot  16px */

/* 
img {
    width: 5.125rem;
    height: 4rem;
    width: 1rem;
    width: 1.093333rem;
    height: 1rem;
} */

/* 如果我们的屏幕超过了 750px  那么我们就按照 750设计稿来走 不会让我们页面超过750px */

@media screen and (min-width: 750px) {
  html {
    font-size: 75px !important;
  }
}

/* search-content */

.search-content {
  display: flex;
  position: fixed;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 10rem;
  height: 1.173333rem;
  background-color: #ffc001;
}

.classify {
  width: 0.586667rem;
  height: 0.933333rem;
  margin: 0.146667rem 0.333333rem 0.133333rem;
  background: url(../images/classify.png) no-repeat;
  background-size: 0.586667rem 0.933333rem;
}

.search {
  flex: 1;
}

.search input {
  outline: none;
  border: 0;
  width: 100%;
  height: 0.88rem;
  font-size: 0.333333rem;
  background-color: #fff2cc;
  margin-top: 0.133333rem;
  border-radius: 0.44rem;
  color: #757575;
  padding-left: 0.733333rem;
}

.login {
  width: 1rem;
  height: 0.933333rem;
  margin: 0.133333rem;
  color: #fff;
  text-align: center;
  line-height: 0.933333rem;
  font-size: 0.333333rem;
}
```

- normalize.css

```css
/*! normalize.css v5.0.0 | MIT License | github.com/necolas/normalize.css */

/**
 * 1. Change the default font family in all browsers (opinionated).
 * 2. Correct the line height in all browsers.
 * 3. Prevent adjustments of font size after orientation changes in
 *    IE on Windows Phone and in iOS.
 */

/* Document
   ========================================================================== */

html {
  font-family: sans-serif; /* 1 */
  line-height: 1.15; /* 2 */
  -ms-text-size-adjust: 100%; /* 3 */
  -webkit-text-size-adjust: 100%; /* 3 */
}

/* Sections
   ========================================================================== */

/**
 * Remove the margin in all browsers (opinionated).
 */

body {
  margin: 0;
}

/**
 * Add the correct display in IE 9-.
 */

article,
aside,
footer,
header,
nav,
section {
  display: block;
}

/**
 * Correct the font size and margin on `h1` elements within `section` and
 * `article` contexts in Chrome, Firefox, and Safari.
 */

h1 {
  font-size: 2em;
  margin: 0.67em 0;
}

/* Grouping content
   ========================================================================== */

/**
 * Add the correct display in IE 9-.
 * 1. Add the correct display in IE.
 */

figcaption,
figure,
main {
  /* 1 */
  display: block;
}

/**
 * Add the correct margin in IE 8.
 */

figure {
  margin: 1em 40px;
}

/**
 * 1. Add the correct box sizing in Firefox.
 * 2. Show the overflow in Edge and IE.
 */

hr {
  box-sizing: content-box; /* 1 */
  height: 0; /* 1 */
  overflow: visible; /* 2 */
}

/**
 * 1. Correct the inheritance and scaling of font size in all browsers.
 * 2. Correct the odd `em` font sizing in all browsers.
 */

pre {
  font-family: monospace, monospace; /* 1 */
  font-size: 1em; /* 2 */
}

/* Text-level semantics
   ========================================================================== */

/**
 * 1. Remove the gray background on active links in IE 10.
 * 2. Remove gaps in links underline in iOS 8+ and Safari 8+.
 */

a {
  background-color: transparent; /* 1 */
  -webkit-text-decoration-skip: objects; /* 2 */
}

/**
 * Remove the outline on focused links when they are also active or hovered
 * in all browsers (opinionated).
 */

a:active,
a:hover {
  outline-width: 0;
}

/**
 * 1. Remove the bottom border in Firefox 39-.
 * 2. Add the correct text decoration in Chrome, Edge, IE, Opera, and Safari.
 */

abbr[title] {
  border-bottom: none; /* 1 */
  text-decoration: underline; /* 2 */
  text-decoration: underline dotted; /* 2 */
}

/**
 * Prevent the duplicate application of `bolder` by the next rule in Safari 6.
 */

b,
strong {
  font-weight: inherit;
}

/**
 * Add the correct font weight in Chrome, Edge, and Safari.
 */

b,
strong {
  font-weight: bolder;
}

/**
 * 1. Correct the inheritance and scaling of font size in all browsers.
 * 2. Correct the odd `em` font sizing in all browsers.
 */

code,
kbd,
samp {
  font-family: monospace, monospace; /* 1 */
  font-size: 1em; /* 2 */
}

/**
 * Add the correct font style in Android 4.3-.
 */

dfn {
  font-style: italic;
}

/**
 * Add the correct background and color in IE 9-.
 */

mark {
  background-color: #ff0;
  color: #000;
}

/**
 * Add the correct font size in all browsers.
 */

small {
  font-size: 80%;
}

/**
 * Prevent `sub` and `sup` elements from affecting the line height in
 * all browsers.
 */

sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}

sub {
  bottom: -0.25em;
}

sup {
  top: -0.5em;
}

/* Embedded content
   ========================================================================== */

/**
 * Add the correct display in IE 9-.
 */

audio,
video {
  display: inline-block;
}

/**
 * Add the correct display in iOS 4-7.
 */

audio:not([controls]) {
  display: none;
  height: 0;
}

/**
 * Remove the border on images inside links in IE 10-.
 */

img {
  border-style: none;
}

/**
 * Hide the overflow in IE.
 */

svg:not(:root) {
  overflow: hidden;
}

/* Forms
   ========================================================================== */

/**
 * 1. Change the font styles in all browsers (opinionated).
 * 2. Remove the margin in Firefox and Safari.
 */

button,
input,
optgroup,
select,
textarea {
  font-family: sans-serif; /* 1 */
  font-size: 100%; /* 1 */
  line-height: 1.15; /* 1 */
  margin: 0; /* 2 */
}

/**
 * Show the overflow in IE.
 * 1. Show the overflow in Edge.
 */

button,
input {
  /* 1 */
  overflow: visible;
}

/**
 * Remove the inheritance of text transform in Edge, Firefox, and IE.
 * 1. Remove the inheritance of text transform in Firefox.
 */

button,
select {
  /* 1 */
  text-transform: none;
}

/**
 * 1. Prevent a WebKit bug where (2) destroys native `audio` and `video`
 *    controls in Android 4.
 * 2. Correct the inability to style clickable types in iOS and Safari.
 */

button,
html [type="button"], /* 1 */
[type="reset"],
[type="submit"] {
  -webkit-appearance: button; /* 2 */
}

/**
 * Remove the inner border and padding in Firefox.
 */

button::-moz-focus-inner,
[type="button"]::-moz-focus-inner,
[type="reset"]::-moz-focus-inner,
[type="submit"]::-moz-focus-inner {
  border-style: none;
  padding: 0;
}

/**
 * Restore the focus styles unset by the previous rule.
 */

button:-moz-focusring,
[type="button"]:-moz-focusring,
[type="reset"]:-moz-focusring,
[type="submit"]:-moz-focusring {
  outline: 1px dotted ButtonText;
}

/**
 * Change the border, margin, and padding in all browsers (opinionated).
 */

fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}

/**
 * 1. Correct the text wrapping in Edge and IE.
 * 2. Correct the color inheritance from `fieldset` elements in IE.
 * 3. Remove the padding so developers are not caught out when they zero out
 *    `fieldset` elements in all browsers.
 */

legend {
  box-sizing: border-box; /* 1 */
  color: inherit; /* 2 */
  display: table; /* 1 */
  max-width: 100%; /* 1 */
  padding: 0; /* 3 */
  white-space: normal; /* 1 */
}

/**
 * 1. Add the correct display in IE 9-.
 * 2. Add the correct vertical alignment in Chrome, Firefox, and Opera.
 */

progress {
  display: inline-block; /* 1 */
  vertical-align: baseline; /* 2 */
}

/**
 * Remove the default vertical scrollbar in IE.
 */

textarea {
  overflow: auto;
}

/**
 * 1. Add the correct box sizing in IE 10-.
 * 2. Remove the padding in IE 10-.
 */

[type="checkbox"],
[type="radio"] {
  box-sizing: border-box; /* 1 */
  padding: 0; /* 2 */
}

/**
 * Correct the cursor style of increment and decrement buttons in Chrome.
 */

[type="number"]::-webkit-inner-spin-button,
[type="number"]::-webkit-outer-spin-button {
  height: auto;
}

/**
 * 1. Correct the odd appearance in Chrome and Safari.
 * 2. Correct the outline style in Safari.
 */

[type="search"] {
  -webkit-appearance: textfield; /* 1 */
  outline-offset: -2px; /* 2 */
}

/**
 * Remove the inner padding and cancel buttons in Chrome and Safari on macOS.
 */

[type="search"]::-webkit-search-cancel-button,
[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}

/**
 * 1. Correct the inability to style clickable types in iOS and Safari.
 * 2. Change font properties to `inherit` in Safari.
 */

::-webkit-file-upload-button {
  -webkit-appearance: button; /* 1 */
  font: inherit; /* 2 */
}

/* Interactive
   ========================================================================== */

/*
 * Add the correct display in IE 9-.
 * 1. Add the correct display in Edge, IE, and Firefox.
 */

details, /* 1 */
menu {
  display: block;
}

/*
 * Add the correct display in all browsers.
 */

summary {
  display: list-item;
}

/* Scripting
   ========================================================================== */

/**
 * Add the correct display in IE 9-.
 */

canvas {
  display: inline-block;
}

/**
 * Add the correct display in IE.
 */

template {
  display: none;
}

/* Hidden
   ========================================================================== */

/**
 * Add the correct display in IE 10-.
 */

[hidden] {
  display: none;
}
```

- flexible.js

```javascript
(function flexible(window, document) {
  var docEl = document.documentElement;
  var dpr = window.devicePixelRatio || 1;

  // adjust body font size
  function setBodyFontSize() {
    if (document.body) {
      document.body.style.fontSize = 12 * dpr + "px";
    } else {
      document.addEventListener("DOMContentLoaded", setBodyFontSize);
    }
  }
  setBodyFontSize();

  // set 1rem = viewWidth / 10
  function setRemUnit() {
    var rem = docEl.clientWidth / 10;
    docEl.style.fontSize = rem + "px";
  }

  setRemUnit();

  // reset rem unit on page resize
  window.addEventListener("resize", setRemUnit);
  window.addEventListener("pageshow", function (e) {
    if (e.persisted) {
      setRemUnit();
    }
  });

  // detect 0.5px supports
  if (dpr >= 2) {
    var fakeBody = document.createElement("body");
    var testElement = document.createElement("div");
    testElement.style.border = ".5px solid transparent";
    fakeBody.appendChild(testElement);
    docEl.appendChild(fakeBody);
    if (testElement.offsetHeight === 1) {
      docEl.classList.add("hairlines");
    }
    docEl.removeChild(fakeBody);
  }
})(window, document);
```

- index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport"
        content="width=device-width, user-scalable=no,initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">

    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="css/normalize.css">
    <link rel="stylesheet" href="css/index.css">
    <!-- 引入我们的flexible.js 文件 -->
    <script src="js/flexible.js"></script>
    <title>Document</title>
</head>

<body>
    <div class="search-content">
        <a href="#" class="classify"></a>
        <div class="search">
            <form action="">
                <input type="search" value="rem适配方案2很开心哦">
            </form>
        </div>
        <a href="#" class="login">登录</a>
    </div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210221163023649.png)

![](https://img-blog.csdnimg.cn/20210221163023750.png)

## 6.3 VSCode px 转换 rem 插件 cssrem

- 这是一个神奇的插件

![](https://img-blog.csdnimg.cn/20210221014001958.png)

![](https://img-blog.csdnimg.cn/20210221014002394.png)

- 设置 html字体大小基准值，打开 设置 快捷键是 ctrl + 逗号

![](https://img-blog.csdnimg.cn/20210221014002424.png)

![](https://img-blog.csdnimg.cn/2021022101400350.png)

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
