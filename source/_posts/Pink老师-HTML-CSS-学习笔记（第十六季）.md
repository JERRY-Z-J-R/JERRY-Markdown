---
title: Pink老师 HTML CSS 学习笔记（第十六季）
date: 2021-02-20 19:03:14
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

# Pink老师 HTML CSS 学习笔记（第十六季）

# 【移动WEB开发之flex布局】

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Pink老师 HTML CSS 学习笔记（第十六季）](#pink%E8%80%81%E5%B8%88-html-css-%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%E7%AC%AC%E5%8D%81%E5%85%AD%E5%AD%A3)
- [【移动WEB开发之flex布局】](#%E7%A7%BB%E5%8A%A8web%E5%BC%80%E5%8F%91%E4%B9%8Bflex%E5%B8%83%E5%B1%80)
- [一、flex 布局体验](#%E4%B8%80flex-%E5%B8%83%E5%B1%80%E4%BD%93%E9%AA%8C)
  - [1.1 传统布局与flex布局](#11-%E4%BC%A0%E7%BB%9F%E5%B8%83%E5%B1%80%E4%B8%8Eflex%E5%B8%83%E5%B1%80)
  - [1.2 初体验](#12-%E5%88%9D%E4%BD%93%E9%AA%8C)
- [二、flex 布局原理](#%E4%BA%8Cflex-%E5%B8%83%E5%B1%80%E5%8E%9F%E7%90%86)
  - [2.1 布局原理](#21-%E5%B8%83%E5%B1%80%E5%8E%9F%E7%90%86)
- [三、flex 布局父项常见属性](#%E4%B8%89flex-%E5%B8%83%E5%B1%80%E7%88%B6%E9%A1%B9%E5%B8%B8%E8%A7%81%E5%B1%9E%E6%80%A7)
  - [3.1 常见父项属性](#31-%E5%B8%B8%E8%A7%81%E7%88%B6%E9%A1%B9%E5%B1%9E%E6%80%A7)
  - [3.2 flex-direction 设置主轴的方向](#32-flex-direction-%E8%AE%BE%E7%BD%AE%E4%B8%BB%E8%BD%B4%E7%9A%84%E6%96%B9%E5%90%91)
  - [3.3 justify-content 设置主轴上的子元素排列方式](#33-justify-content-%E8%AE%BE%E7%BD%AE%E4%B8%BB%E8%BD%B4%E4%B8%8A%E7%9A%84%E5%AD%90%E5%85%83%E7%B4%A0%E6%8E%92%E5%88%97%E6%96%B9%E5%BC%8F)
  - [3.4 flex-wrap 设置子元素是否换行](#34-flex-wrap-%E8%AE%BE%E7%BD%AE%E5%AD%90%E5%85%83%E7%B4%A0%E6%98%AF%E5%90%A6%E6%8D%A2%E8%A1%8C)
  - [3.5 align-items 设置侧轴上的子元素排列方式（单行 ）](#35-align-items-%E8%AE%BE%E7%BD%AE%E4%BE%A7%E8%BD%B4%E4%B8%8A%E7%9A%84%E5%AD%90%E5%85%83%E7%B4%A0%E6%8E%92%E5%88%97%E6%96%B9%E5%BC%8F%E5%8D%95%E8%A1%8C-)
  - [3.6 align-content 设置侧轴上的子元素的排列方式（多行）](#36-align-content-%E8%AE%BE%E7%BD%AE%E4%BE%A7%E8%BD%B4%E4%B8%8A%E7%9A%84%E5%AD%90%E5%85%83%E7%B4%A0%E7%9A%84%E6%8E%92%E5%88%97%E6%96%B9%E5%BC%8F%E5%A4%9A%E8%A1%8C)
  - [3.7 align-content 和 align-items 区别](#37-align-content-%E5%92%8C-align-items-%E5%8C%BA%E5%88%AB)
  - [3.8 flex-flow](#38-flex-flow)
- [四、flex 布局子项常见属性](#%E5%9B%9Bflex-%E5%B8%83%E5%B1%80%E5%AD%90%E9%A1%B9%E5%B8%B8%E8%A7%81%E5%B1%9E%E6%80%A7)
  - [4.1 flex 属性](#41-flex-%E5%B1%9E%E6%80%A7)
  - [4.2 align-self 控制子项自己在侧轴上的排列方式](#42-align-self-%E6%8E%A7%E5%88%B6%E5%AD%90%E9%A1%B9%E8%87%AA%E5%B7%B1%E5%9C%A8%E4%BE%A7%E8%BD%B4%E4%B8%8A%E7%9A%84%E6%8E%92%E5%88%97%E6%96%B9%E5%BC%8F)
  - [4.3 order 属性定义项目的排列顺序](#43-order-%E5%B1%9E%E6%80%A7%E5%AE%9A%E4%B9%89%E9%A1%B9%E7%9B%AE%E7%9A%84%E6%8E%92%E5%88%97%E9%A1%BA%E5%BA%8F)
- [五、携程网首页案例制作](#%E4%BA%94%E6%90%BA%E7%A8%8B%E7%BD%91%E9%A6%96%E9%A1%B5%E6%A1%88%E4%BE%8B%E5%88%B6%E4%BD%9C)
  - [5.1 技术选型](#51-%E6%8A%80%E6%9C%AF%E9%80%89%E5%9E%8B)
  - [5.2 搭建相关文件夹结构](#52-%E6%90%AD%E5%BB%BA%E7%9B%B8%E5%85%B3%E6%96%87%E4%BB%B6%E5%A4%B9%E7%BB%93%E6%9E%84)
  - [5.3 设置视口标签以及引入初始化样式](#53-%E8%AE%BE%E7%BD%AE%E8%A7%86%E5%8F%A3%E6%A0%87%E7%AD%BE%E4%BB%A5%E5%8F%8A%E5%BC%95%E5%85%A5%E5%88%9D%E5%A7%8B%E5%8C%96%E6%A0%B7%E5%BC%8F)
  - [5.4 常用初始化样式](#54-%E5%B8%B8%E7%94%A8%E5%88%9D%E5%A7%8B%E5%8C%96%E6%A0%B7%E5%BC%8F)
  - [5.5 常见模块命名](#55-%E5%B8%B8%E8%A7%81%E6%A8%A1%E5%9D%97%E5%91%BD%E5%90%8D)
  - [5.6 常见flex布局思路](#56-%E5%B8%B8%E8%A7%81flex%E5%B8%83%E5%B1%80%E6%80%9D%E8%B7%AF)
  - [5.7 背景线性渐变](#57-%E8%83%8C%E6%99%AF%E7%BA%BF%E6%80%A7%E6%B8%90%E5%8F%98)
  - [5.8 案例结构和内容](#58-%E6%A1%88%E4%BE%8B%E7%BB%93%E6%9E%84%E5%92%8C%E5%86%85%E5%AE%B9)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


# 一、flex 布局体验

## 1.1 传统布局与flex布局

![](https://img-blog.csdnimg.cn/20210220191110726.png)

## 1.2 初体验

![](https://img-blog.csdnimg.cn/2021022019120574.png)

- 1、搭建 HTML 结构

```html
<div>
	<span>1</span>
	<span>2</span>
	<span>3</span>
</div>
```

里面的3个 `span` 是行内元素

- 2、CSS 样式

1. `span` 直接给宽度和高度，背景颜色，还有蓝色边框

2. 给 `div` 只需要添加 “`display：flex`” 即可

![](https://img-blog.csdnimg.cn/20210220191507457.png)

# 二、flex 布局原理

## 2.1 布局原理

`flex` 是 `flexible Box` 的缩写，意为 "`弹性布局`"，用来为盒状模型提供最大的灵活性，任何一个容器都可以指定为 `flex` 布局

- 当我们为父盒子设为 `flex` 布局以后，子元素的 `float`、`clear` 和 `vertical-align` 属性将失效

- `伸缩布局` = `弹性布局` = `伸缩盒布局` = `弹性盒布局` = `flex 布局`

采用 `flex` 布局的元素，称为 `flex 容器`（`flex container`），简称 "`容器`"，它的所有子元素自动成为容器成员，称为 `flex 项目`（`flex item`），简称 "`项目`"

- 体验中 `div` 就是 `flex` 父容器
- 体验中 `span` 就是 子容器 `flex` 项目
- 子容器可以横向排列也可以纵向排列

总结 `flex` 布局原理：
就是通过给父盒子添加 `flex` 属性，来控制子盒子的位置和排列方式

![](https://img-blog.csdnimg.cn/20210220192119184.png)

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>01-flex布局体验</title>
    <style>
        div {
            display: flex;
            width: 80%;
            height: 300px;
            background-color: pink;
            justify-content: space-around;
        }

        div span {
            /* width: 150px; */
            height: 100px;
            background-color: purple;
            margin-right: 5px;
            flex: 1;
        }
    </style>
</head>

<body>
    <div>
        <span>1</span>
        <span>2</span>
        <span>3</span>
    </div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210220214215540.png)

![](https://img-blog.csdnimg.cn/20210220214215588.png)

# 三、flex 布局父项常见属性

## 3.1 常见父项属性

以下由6个属性是对父元素设置的

- `flex-direction`：设置主轴的方向
- `justify-content`：设置主轴上的子元素排列方式
- `flex-wrap`：设置子元素是否换行
- `align-content`：设置侧轴上的子元素的排列方式（多行）
- `align-items`：设置侧轴上的子元素排列方式（单行）
- `flex-flow`：复合属性，相当于同时设置了 flex-direction 和 flex-wrap

## 3.2 flex-direction 设置主轴的方向

- 1、主轴与侧轴

在 flex 布局中，是分为主轴和侧轴两个方向，同样的叫法有 ： 行和列、x 轴 和 y 轴

`默认主轴方向就是 x 轴方向，水平向右`

`默认侧轴方向就是 y 轴方向，水平向下`

![](https://img-blog.csdnimg.cn/20210220192530805.png)

- 2、属性值

`flex-direction` 属性决定主轴的方向（即项目的排列方向）

注意： 主轴和侧轴是会变化的，就看 `flex-direction` 设置谁为主轴，剩下的就是侧轴。而我们的子元素是跟着主轴来排列的

![](https://img-blog.csdnimg.cn/20210220192720148.png)

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>02-flex主轴方向</title>
    <style>
        div {
            /* 给父级添加flex属性 */
            display: flex;
            width: 800px;
            height: 300px;
            background-color: pink;
            /* 默认的主轴是 x 轴 行 row  那么y轴就是侧轴喽 */
            /* 我们的元素是跟着主轴来排列的 */
            /* flex-direction: row; */
            /* 简单了解 翻转 */
            /* flex-direction: row-reverse; */
            /* 我们可以把我们的主轴设置为 y轴 那么 x 轴就成了侧轴 */
            flex-direction: column;
        }

        div span {
            width: 150px;
            height: 100px;
            background-color: purple;
        }
    </style>
</head>

<body>
    <div>
        <span>1</span>
        <span>2</span>
        <span>3</span>
    </div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210220214556162.png)

![](https://img-blog.csdnimg.cn/20210220214556323.png)

## 3.3 justify-content 设置主轴上的子元素排列方式

`justify-content` 属性定义了项目在主轴上的对齐方式

**注意：** 使用这个属性之前一定要确定好主轴是哪个

![](https://img-blog.csdnimg.cn/20210220192910392.png)

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>03-flex设置主轴上的子元素排列方式1</title>
    <style>
        div {
            display: flex;
            width: 800px;
            height: 300px;
            background-color: pink;
            /* 默认的主轴是 x 轴 row */
            flex-direction: row;
            /* justify-content: 是设置主轴上子元素的排列方式 */
            /* justify-content: flex-start; */
            /* justify-content: flex-end; */
            /* 让我们子元素居中对齐 */
            /* justify-content: center; */
            /* 平分剩余空间 */
            /* justify-content: space-around; */
            /* 先两边贴边， 在分配剩余的空间 */
            justify-content: space-between;
        }

        div span {
            width: 150px;
            height: 100px;
            background-color: purple;
        }
    </style>
</head>

<body>
    <div>
        <span>1</span>
        <span>2</span>
        <span>3</span>
        <span>4</span>
    </div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/2021022021475389.png)

![](https://img-blog.csdnimg.cn/20210220214753225.png)

---

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>04-flex设置主轴上的子元素排列方式2</title>
    <style>
        div {
            display: flex;
            width: 800px;
            height: 400px;
            background-color: pink;
            /* 我们现在的主轴是y轴 */
            flex-direction: column;
            /* justify-content: center; */
            justify-content: space-between;
        }

        div span {
            width: 150px;
            height: 100px;
            background-color: purple;
        }
    </style>
</head>

<body>
    <div>
        <span>1</span>
        <span>2</span>
        <span>3</span>
    </div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210220214909690.png)

![](https://img-blog.csdnimg.cn/20210220214909939.png)

## 3.4 flex-wrap 设置子元素是否换行

默认情况下，项目都排在一条线（又称 “`轴线`” ）上，`flex-wrap` 属性定义，`flex` 布局中默认是不换行的

![](https://img-blog.csdnimg.cn/20210220193057918.png)

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>05-flex-wrap子元素是否换行</title>
    <style>
        div {
            display: flex;
            width: 600px;
            height: 400px;
            background-color: pink;
            /* flex布局中，默认的子元素是不换行的， 如果装不开，会缩小子元素的宽度，放到父元素里面  */
            /* flex-wrap: nowrap; */
            flex-wrap: wrap;
        }

        div span {
            width: 150px;
            height: 100px;
            background-color: purple;
            color: #fff;
            margin: 10px;
        }
    </style>
</head>

<body>
    <div>
        <span>1</span>
        <span>2</span>
        <span>3</span>
        <span>4</span>
        <span>5</span>
    </div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210220215052734.png)

![](https://img-blog.csdnimg.cn/20210220215052919.png)

## 3.5 align-items 设置侧轴上的子元素排列方式（单行 ）

该属性是控制子项在侧轴（默认是 y轴）上的排列方式 在子项为单项（单行）的时候使用

![](https://img-blog.csdnimg.cn/20210220193208472.png)

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>06-flex设置侧轴上的子元素排列方式</title>
    <style>
        div {
            display: flex;
            width: 800px;
            height: 400px;
            background-color: pink;
            /* 默认的主轴是 x 轴 row */
            flex-direction: column;
            justify-content: center;
            /* 我们需要一个侧轴居中 */
            /* 拉伸，但是子盒子不要给高度 */
            /* align-items: stretch; */
            align-items: center;
            /* align-content: center; */
        }

        div span {
            width: 150px;
            height: 100px;
            background-color: purple;
            color: #fff;
            margin: 10px;
        }
    </style>
</head>

<body>
    <div>
        <span>1</span>
        <span>2</span>
        <span>3</span>
    </div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210220215748310.png)

![](https://img-blog.csdnimg.cn/20210220215748403.png)


## 3.6 align-content 设置侧轴上的子元素的排列方式（多行）

设置子项在侧轴上的排列方式 并且只能用于子项出现换行的情况（多行），在单行下是没有效果的

![](https://img-blog.csdnimg.cn/20210220193332954.png)

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>07-flex设置侧轴对齐方式（多行）</title>
    <style>
        div {
            display: flex;
            width: 800px;
            height: 400px;
            background-color: pink;
            /* 换行 */
            flex-wrap: wrap;
            /* 因为有了换行，此时我们侧轴上控制子元素的对齐方式我们用 align-content */
            /* align-content: flex-start; */
            /* align-content: center; */
            /* align-content: space-between; */
            align-content: space-around;
        }

        div span {
            width: 150px;
            height: 100px;
            background-color: purple;
            color: #fff;
            margin: 10px;
        }
    </style>
</head>

<body>
    <div>
        <span>1</span>
        <span>2</span>
        <span>3</span>
        <span>4</span>
        <span>5</span>
        <span>6</span>
    </div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210220215909242.png)

![](https://img-blog.csdnimg.cn/20210220215909650.png)


## 3.7 align-content 和 align-items 区别

- `align-items` 适用于单行情况下， 只有上对齐、下对齐、居中 和 拉伸
- `align-content` 适应于换行（多行）的情况下（单行情况下无效）， 可以设置 上对齐、下对齐、居中、拉伸以及平均分配剩余空间等属性值
- 总结就是单行找 `align-items` 多行找 `align-content`

![](https://img-blog.csdnimg.cn/20210220193730664.png)

## 3.8 flex-flow

flex-flow 属性是 flex-direction 和 flex-wrap 属性的复合属性

`flex-flow:row wrap;`

- `flex-direction`：设置主轴的方向
- `justify-content`：设置主轴上的子元素排列方式
- `flex-wrap`：设置子元素是否换行
- `align-content`：设置侧轴上的子元素的排列方式（多行）
- `align-items`：设置侧轴上的子元素排列方式（单行）
- `flex-flow`：复合属性，相当于同时设置了 `flex-direction` 和 `flex-wrap`

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>08-flex-flow复合属性</title>
    <style>
        div {
            display: flex;
            width: 600px;
            height: 300px;
            background-color: pink;
            /* flex-direction: column;
            flex-wrap: wrap; */
            /* 把设置主轴方向和是否换行（换列）简写 */
            flex-flow: column wrap;
        }

        div span {
            width: 150px;
            height: 100px;
            background-color: purple;
        }
    </style>
</head>

<body>
    <div>
        <span>1</span>
        <span>2</span>
        <span>3</span>
        <span>4</span>
        <span>5</span>
    </div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210220221021622.png)

![](https://img-blog.csdnimg.cn/20210220221021667.png)

# 四、flex 布局子项常见属性

- `flex` 子项目占的份数
- `align-self` 控制子项自己在侧轴的排列方式
- `order` 属性定义子项的排列顺序（前后顺序）

## 4.1 flex 属性

`flex` 属性定义子项目分配剩余空间，用 `flex` 来表示占多少份数

```css
.item {
	flex: <number>; 	/* default 0 */
}
```

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>09-flex子项flex份数</title>
    <style>
        section {
            display: flex;
            width: 60%;
            height: 150px;
            background-color: pink;
            margin: 0 auto;
        }

        section div:nth-child(1) {
            width: 100px;
            height: 150px;
            background-color: red;
        }

        section div:nth-child(2) {
            flex: 1;
            background-color: green;
        }

        section div:nth-child(3) {
            width: 100px;
            height: 150px;
            background-color: blue;
        }

        p {
            display: flex;
            width: 60%;
            height: 150px;
            background-color: pink;
            margin: 100px auto;
        }

        p span {
            flex: 1;
        }

        p span:nth-child(2) {
            flex: 2;
            background-color: purple;
        }
    </style>
</head>

<body>
    <section>
        <div></div>
        <div></div>
        <div></div>
    </section>
    <p>
        <span>1</span>
        <span>2</span>
        <span>3</span>
    </p>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210220221327634.png)

![](https://img-blog.csdnimg.cn/20210220221327738.png)

## 4.2 align-self 控制子项自己在侧轴上的排列方式

`align-self` 属性允许单个项目有与其他项目不一样的对齐方式，可覆盖 `align-items` 属性，默认值为 `auto`，表示继承父元素的 `align-items` 属性，如果没有父元素，则等同于  `stretch`

```css
span:nth-child(2) {
	/* 设置自己在侧轴上的排列方式 */
	align-self: flex-end;
}
```

## 4.3 order 属性定义项目的排列顺序

数值越小，排列越靠前，默认为 `0`

注意：和 `z-index` 不一样

```css
.item {
	order: <number>;
}
```

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>10-align-self和order</title>
    <style>
        div {
            display: flex;
            width: 80%;
            height: 300px;
            background-color: pink;
            /* 让三个子盒子沿着侧轴底侧对齐 */
            /* align-items: flex-end; */
            /* 我们想只让3号盒子下来底侧 */
        }

        div span {
            width: 150px;
            height: 100px;
            background-color: purple;
            margin-right: 5px;
        }

        div span:nth-child(2) {
            /* 默认是0   -1比0小所以在前面 */
            order: -1;
        }

        div span:nth-child(3) {
            align-self: flex-end;
        }
    </style>
</head>

<body>
    <div>
        <span>1</span>
        <span>2</span>
        <span>3</span>
    </div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210220221201393.png)

![](https://img-blog.csdnimg.cn/20210220221201612.png)

# 五、携程网首页案例制作

- 访问地址：[m.ctrip.com](m.ctrip.com)

![](https://img-blog.csdnimg.cn/20210220212306711.png)

## 5.1 技术选型

方案：我们采取单独制作移动页面方案
技术：布局采取 `flex` 布局

## 5.2 搭建相关文件夹结构

![](https://img-blog.csdnimg.cn/20210220212547528.png)

## 5.3 设置视口标签以及引入初始化样式

```html
<meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
<link rel="stylesheet" href="css/normalize.css">
<link rel="stylesheet" href="css/index.css">
```

## 5.4 常用初始化样式

```css
body {
	max-width: 540px;
	min-width: 320px;
	margin: 0 auto;
	font: normal 14px/1.5 Tahoma, "Lucida Grande", Verdana, "Microsoft 			Yahei", STXihei, hei;
	color: #000;
	background: #f2f2f2;
	overflow-x: hidden;
	-webkit-tap-highlight-color: transparent;
}
```

## 5.5 常见模块命名

![](https://img-blog.csdnimg.cn/20210220213005549.png)

![](https://img-blog.csdnimg.cn/2021022021310362.png)

## 5.6 常见flex布局思路

![](https://img-blog.csdnimg.cn/20210220213308429.png)

## 5.7 背景线性渐变

![](https://img-blog.csdnimg.cn/20210220213308356.png)

**语法1：**

```css
background: linear-gradient(起始方向, 颜色1, 颜色2, ...);
background: -webkit-linear-gradient(left, red , blue);
background: -webkit-linear-gradient(left top, red , blue);
```

背景渐变必须添加浏览器私有前缀
起始方向可以是： 方位名词 或者 度数，如果省略默认就是 `top`

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>11-背景线性渐变</title>
    <style>
        div {
            width: 600px;
            height: 200px;
            /* 背景渐变必须添加浏览器私有前缀 */
            /* background: -webkit-linear-gradient(left, red, blue); */
            /* background: -webkit-linear-gradient(red, blue); */
            background: -webkit-linear-gradient(top left, red, blue);
        }
    </style>
</head>

<body>
    <div></div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210220220100438.png)

![](https://img-blog.csdnimg.cn/20210220220100646.png)

## 5.8 案例结构和内容

![](https://img-blog.csdnimg.cn/20210220221507604.png)

![](https://img-blog.csdnimg.cn/20210220221507566.png)

![](https://img-blog.csdnimg.cn/20210220221507583.png)

![](https://img-blog.csdnimg.cn/20210220221507611.png)

- index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="css/normalize.css">
    <link rel="stylesheet" href="css/index.css">
    <title>携程在手，说走就走</title>
</head>

<body>
    <!-- 顶部搜索 -->
    <div class="search-index">
        <div class="search">搜索:目的地/酒店/景点/航班号</div>
        <a href="#" class="user">我 的</a>
    </div>
    <!-- 焦点图模块 -->
    <div class="focus">
        <img src="upload/focus.jpg" alt="">
    </div>
    <!-- 局部导航栏 -->
    <ul class="local-nav">
        <li>
            <a href="#" title="景点·玩乐">
                <span class="local-nav-icon-icon1"></span>
                <span>景点·玩乐</span>
            </a>
        </li>
        <li>
            <a href="#" title="景点·玩乐">
                <span class="local-nav-icon-icon2"></span>
                <span>景点·玩乐</span>
            </a>
        </li>
        <li>
            <a href="#" title="景点·玩乐">
                <span class="local-nav-icon-icon3"></span>
                <span>景点·玩乐</span>
            </a>
        </li>
        <li>
            <a href="#" title="景点·玩乐">
                <span class="local-nav-icon-icon4"></span>
                <span>景点·玩乐</span>
            </a>
        </li>
        <li>
            <a href="#" title="景点·玩乐">
                <span class="local-nav-icon-icon5"></span>
                <span>景点·玩乐</span>
            </a>
        </li>

    </ul>

    <!-- 主导航栏 -->
    <nav>
        <div class="nav-common">
            <div class="nav-items">
                <a href="#">海外酒店</a>
            </div>
            <div class="nav-items">
                <a href="#">海外酒店</a>
                <a href="#">特价酒店</a>
            </div>
            <div class="nav-items">
                <a href="#">海外酒店</a>
                <a href="#">特价酒店</a>
            </div>
        </div>
        <div class="nav-common">
            <div class="nav-items">
                <a href="#">海外酒店</a>
            </div>
            <div class="nav-items">
                <a href="#">海外酒店</a>
                <a href="#">特价酒店</a>
            </div>
            <div class="nav-items">
                <a href="#">海外酒店</a>
                <a href="#">特价酒店</a>
            </div>
        </div>
        <div class="nav-common">
            <div class="nav-items">
                <a href="#">海外酒店</a>
            </div>
            <div class="nav-items">
                <a href="#">海外酒店</a>
                <a href="#">特价酒店</a>
            </div>
            <div class="nav-items">
                <a href="#">海外酒店</a>
                <a href="#">特价酒店</a>
            </div>
        </div>

    </nav>
    <!-- 侧导航栏 -->
    <ul class="subnav-entry">
        <li>
            <a href="#">
                <span class="subnav-entry-icon"></span>
                <span>电话费</span>
            </a>
        </li>
        <li>
            <a href="#">
                <span class="subnav-entry-icon"></span>
                <span>电话费</span>
            </a>
        </li>
        <li>
            <a href="#">
                <span class="subnav-entry-icon"></span>
                <span>电话费</span>
            </a>
        </li>
        <li>
            <a href="#">
                <span class="subnav-entry-icon"></span>
                <span>电话费</span>
            </a>
        </li>
        <li>
            <a href="#">
                <span class="subnav-entry-icon"></span>
                <span>电话费</span>
            </a>
        </li>
        <li>
            <a href="#">
                <span class="subnav-entry-icon"></span>
                <span>电话费</span>
            </a>
        </li>
        <li>
            <a href="#">
                <span class="subnav-entry-icon"></span>
                <span>电话费</span>
            </a>
        </li>
        <li>
            <a href="#">
                <span class="subnav-entry-icon"></span>
                <span>电话费</span>
            </a>
        </li>
        <li>
            <a href="#">
                <span class="subnav-entry-icon"></span>
                <span>电话费</span>
            </a>
        </li>
        <li>
            <a href="#">
                <span class="subnav-entry-icon"></span>
                <span>电话费</span>
            </a>
        </li>

    </ul>

    <!-- 销售模块 -->
    <div class="sales-box">
        <div class="sales-hd">
            <h2>热门活动</h2>
            <a href="#" class="more">获取更多福利</a>
        </div>
        <div class="sales-bd">
            <div class="row">
                <a href="#">
                    <img src="upload/pic1.jpg" alt="">
                </a>
                <a href="#">
                    <img src="upload/pic2.jpg" alt="">

                </a>
            </div>
            <div class="row">
                <a href="#">
                    <img src="upload/pic3.jpg" alt="">
                </a>
                <a href="#">
                    <img src="upload/pic4.jpg" alt="">

                </a>
            </div>
            <div class="row">
                <a href="#">
                    <img src="upload/pic5.jpg" alt="">
                </a>
                <a href="#">
                    <img src="upload/pic6.jpg" alt="">

                </a>
            </div>

        </div>
    </div>
</body>

</html>
```

- index.css

```css
body {
  max-width: 540px;
  min-width: 320px;
  margin: 0 auto;
  font: normal 14px/1.5 Tahoma, "Lucida Grande", Verdana, "Microsoft Yahei",
    STXihei, hei;
  color: #000;
  background: #f2f2f2;
  overflow-x: hidden;
  -webkit-tap-highlight-color: transparent;
}

ul {
  list-style: none;
  margin: 0;
  padding: 0;
}

a {
  text-decoration: none;
  color: #222;
}

div {
  box-sizing: border-box;
}

/* 搜索模块 */

.search-index {
  display: flex;
  /* 固定定位跟父级没有关系 它以屏幕为准 */
  position: fixed;
  top: 0;
  left: 50%;
  /* 固定的盒子应该有宽度 */
  -webkit-transform: translateX(-50%);
  transform: translateX(-50%);
  width: 100%;
  min-width: 320px;
  max-width: 540px;
  height: 44px;
  /* background-color: pink; */
  background-color: #f6f6f6;
  border-top: 1px solid #ccc;
  border-bottom: 1px solid #ccc;
}

.search {
  position: relative;
  height: 26px;
  line-height: 24px;
  border: 1px solid #ccc;
  flex: 1;
  font-size: 12px;
  color: #666;
  margin: 7px 10px;
  padding-left: 25px;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

.search::before {
  content: "";
  position: absolute;
  top: 5px;
  left: 5px;
  width: 15px;
  height: 15px;
  background: url(../images/sprite.png) no-repeat -59px -279px;
  background-size: 104px auto;
}

.user {
  width: 44px;
  height: 44px;
  /* background-color: purple; */
  font-size: 12px;
  text-align: center;
  color: #2eaae0;
}

.user::before {
  content: "";
  display: block;
  width: 23px;
  height: 23px;
  background: url(../images/sprite.png) no-repeat -59px -194px;
  background-size: 104px auto;
  margin: 4px auto -2px;
}

/* focus */

.focus {
  padding-top: 44px;
}

.focus img {
  width: 100%;
}

/* local-nav */

.local-nav {
  display: flex;
  height: 64px;
  margin: 3px 4px;
  background-color: #fff;
  border-radius: 8px;
}

.local-nav li {
  flex: 1;
}

.local-nav a {
  display: flex;
  flex-direction: column;
  /* 侧轴居中对齐 因为是单行 */
  align-items: center;
  font-size: 12px;
}

.local-nav li [class^="local-nav-icon"] {
  width: 32px;
  height: 32px;
  background-color: pink;
  margin-top: 8px;
  background: url(../images/localnav_bg.png) no-repeat 0 0;
  background-size: 32px auto;
}

.local-nav li .local-nav-icon-icon2 {
  background-position: 0 -32px;
}

.local-nav li .local-nav-icon-icon3 {
  background-position: 0 -64px;
}

.local-nav li .local-nav-icon-icon4 {
  background-position: 0 -96px;
}

.local-nav li .local-nav-icon-icon5 {
  background-position: 0 -128px;
}

/* nav */

nav {
  overflow: hidden;
  border-radius: 8px;
  margin: 0 4px 3px;
}

.nav-common {
  display: flex;
  height: 88px;
  background-color: pink;
}

.nav-common:nth-child(2) {
  margin: 3px 0;
}

.nav-items {
  /* 不冲突的 */
  flex: 1;
  display: flex;
  flex-direction: column;
}

.nav-items a {
  flex: 1;
  text-align: center;
  line-height: 44px;
  color: #fff;
  font-size: 14px;
  /* 文字阴影 */
  text-shadow: 1px 1px rgba(0, 0, 0, 0.2);
}

.nav-items a:nth-child(1) {
  border-bottom: 1px solid #fff;
}

.nav-items:nth-child(1) a {
  border: 0;
  background: url(../images/hotel.png) no-repeat bottom center;
  background-size: 121px auto;
}

/* -n+2就是选择前面两个元素 */

.nav-items:nth-child(-n + 2) {
  border-right: 1px solid #fff;
}

.nav-common:nth-child(1) {
  background: -webkit-linear-gradient(left, #fa5a55, #fa994d);
}

.nav-common:nth-child(2) {
  background: -webkit-linear-gradient(left, #4b90ed, #53bced);
}

.nav-common:nth-child(3) {
  background: -webkit-linear-gradient(left, #34c2a9, #6cd559);
}

/* subnav-entry */

.subnav-entry {
  display: flex;
  border-radius: 8px;
  background-color: #fff;
  margin: 0 4px;
  flex-wrap: wrap;
  padding: 5px 0;
}

.subnav-entry li {
  /* 里面的子盒子可以写 % 相对于父级来说的 */
  flex: 20%;
}

.subnav-entry a {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.subnav-entry-icon {
  width: 28px;
  height: 28px;
  background-color: pink;
  margin-top: 4px;
  background: url(../images/subnav-bg.png) no-repeat;
  background-size: 28px auto;
}

/* sales-box */

.sales-box {
  border-top: 1px solid #bbb;
  background-color: #fff;
  margin: 4px;
}

.sales-hd {
  position: relative;
  height: 44px;
  border-bottom: 1px solid #ccc;
}

.sales-hd h2 {
  position: relative;
  text-indent: -999px;
  overflow: hidden;
}

.sales-hd h2::after {
  position: absolute;
  top: 5px;
  left: 8px;
  content: "";
  width: 79px;
  height: 15px;
  background: url(../images/hot.png) no-repeat 0 -20px;
  background-size: 79px auto;
}

.more {
  position: absolute;
  right: 5px;
  top: 0px;
  background: -webkit-linear-gradient(left, #ff506c, #ff6bc6);
  border-radius: 15px;
  padding: 3px 20px 3px 10px;
  color: #fff;
}

.more::after {
  content: "";
  position: absolute;
  top: 9px;
  right: 9px;
  width: 7px;
  height: 7px;
  border-top: 2px solid #fff;
  border-right: 2px solid #fff;
  transform: rotate(45deg);
}

.row {
  display: flex;
}

.row a {
  flex: 1;
  border-bottom: 1px solid #eee;
}

.row a:nth-child(1) {
  border-right: 1px solid #eee;
}

.row a img {
  width: 100%;
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

![](https://img-blog.csdnimg.cn/2021022022192058.png)

![](https://img-blog.csdnimg.cn/20210220221919918.png)

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