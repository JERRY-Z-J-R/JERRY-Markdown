---
title: Pink老师 HTML CSS 学习笔记（第十五季）
date: 2021-02-20 15:21:06
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

# Pink老师 HTML CSS 学习笔记（第十五季）

# 【移动WEB开发之流式布局】

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Pink老师 HTML CSS 学习笔记（第十五季）](#pink%E8%80%81%E5%B8%88-html-css-%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%E7%AC%AC%E5%8D%81%E4%BA%94%E5%AD%A3)
- [【移动WEB开发之流式布局】](#%E7%A7%BB%E5%8A%A8web%E5%BC%80%E5%8F%91%E4%B9%8B%E6%B5%81%E5%BC%8F%E5%B8%83%E5%B1%80)
- [一、移动端基础](#%E4%B8%80%E7%A7%BB%E5%8A%A8%E7%AB%AF%E5%9F%BA%E7%A1%80)
  - [1.1 浏览器现状](#11-%E6%B5%8F%E8%A7%88%E5%99%A8%E7%8E%B0%E7%8A%B6)
  - [1.2 手机屏幕现状](#12-%E6%89%8B%E6%9C%BA%E5%B1%8F%E5%B9%95%E7%8E%B0%E7%8A%B6)
  - [1.3 常见移动端屏幕尺寸](#13-%E5%B8%B8%E8%A7%81%E7%A7%BB%E5%8A%A8%E7%AB%AF%E5%B1%8F%E5%B9%95%E5%B0%BA%E5%AF%B8)
  - [1.4 移动端调试方法](#14-%E7%A7%BB%E5%8A%A8%E7%AB%AF%E8%B0%83%E8%AF%95%E6%96%B9%E6%B3%95)
  - [1.5 总结](#15-%E6%80%BB%E7%BB%93)
- [二、视口](#%E4%BA%8C%E8%A7%86%E5%8F%A3)
  - [2.1 布局视口 layout viewport](#21-%E5%B8%83%E5%B1%80%E8%A7%86%E5%8F%A3-layout-viewport)
  - [2.2 视觉视口 visual viewport](#22-%E8%A7%86%E8%A7%89%E8%A7%86%E5%8F%A3-visual-viewport)
  - [2.3 理想视口 ideal viewport](#23-%E7%90%86%E6%83%B3%E8%A7%86%E5%8F%A3-ideal-viewport)
  - [2.4 总结](#24-%E6%80%BB%E7%BB%93)
  - [2.5 meta视口标签](#25-meta%E8%A7%86%E5%8F%A3%E6%A0%87%E7%AD%BE)
  - [2.6 标准的viewport设置](#26-%E6%A0%87%E5%87%86%E7%9A%84viewport%E8%AE%BE%E7%BD%AE)
- [三、二倍图](#%E4%B8%89%E4%BA%8C%E5%80%8D%E5%9B%BE)
  - [3.1 物理像素&物理像素比](#31-%E7%89%A9%E7%90%86%E5%83%8F%E7%B4%A0%E7%89%A9%E7%90%86%E5%83%8F%E7%B4%A0%E6%AF%94)
  - [3.2 多倍图](#32-%E5%A4%9A%E5%80%8D%E5%9B%BE)
  - [3.3 背景缩放 background-size](#33-%E8%83%8C%E6%99%AF%E7%BC%A9%E6%94%BE-background-size)
  - [3.4 多倍图切图 cutterman](#34-%E5%A4%9A%E5%80%8D%E5%9B%BE%E5%88%87%E5%9B%BE-cutterman)
- [四、移动端开发选择](#%E5%9B%9B%E7%A7%BB%E5%8A%A8%E7%AB%AF%E5%BC%80%E5%8F%91%E9%80%89%E6%8B%A9)
  - [4.1 移动端主流方案](#41-%E7%A7%BB%E5%8A%A8%E7%AB%AF%E4%B8%BB%E6%B5%81%E6%96%B9%E6%A1%88)
  - [4.2 单独移动端页面（主流）](#42-%E5%8D%95%E7%8B%AC%E7%A7%BB%E5%8A%A8%E7%AB%AF%E9%A1%B5%E9%9D%A2%E4%B8%BB%E6%B5%81)
  - [4.3 响应式兼容PC移动端](#43-%E5%93%8D%E5%BA%94%E5%BC%8F%E5%85%BC%E5%AE%B9pc%E7%A7%BB%E5%8A%A8%E7%AB%AF)
  - [4.4 总结](#44-%E6%80%BB%E7%BB%93)
- [五、移动端技术解决方案](#%E4%BA%94%E7%A7%BB%E5%8A%A8%E7%AB%AF%E6%8A%80%E6%9C%AF%E8%A7%A3%E5%86%B3%E6%96%B9%E6%A1%88)
  - [5.1 移动端浏览器](#51-%E7%A7%BB%E5%8A%A8%E7%AB%AF%E6%B5%8F%E8%A7%88%E5%99%A8)
  - [5.2 CSS初始化 normalize.css](#52-css%E5%88%9D%E5%A7%8B%E5%8C%96-normalizecss)
  - [5.3 CSS3 盒子模型 box-sizing](#53-css3-%E7%9B%92%E5%AD%90%E6%A8%A1%E5%9E%8B-box-sizing)
  - [5.4 特殊样式](#54-%E7%89%B9%E6%AE%8A%E6%A0%B7%E5%BC%8F)
- [六、移动端常见布局](#%E5%85%AD%E7%A7%BB%E5%8A%A8%E7%AB%AF%E5%B8%B8%E8%A7%81%E5%B8%83%E5%B1%80)
  - [6.1 流式布局（百分比布局）](#61-%E6%B5%81%E5%BC%8F%E5%B8%83%E5%B1%80%E7%99%BE%E5%88%86%E6%AF%94%E5%B8%83%E5%B1%80)
  - [6.2 案例：京东移动端首页](#62-%E6%A1%88%E4%BE%8B%E4%BA%AC%E4%B8%9C%E7%A7%BB%E5%8A%A8%E7%AB%AF%E9%A6%96%E9%A1%B5)
- [七、总结](#%E4%B8%83%E6%80%BB%E7%BB%93)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# 一、移动端基础

## 1.1 浏览器现状

![](https://img-blog.csdnimg.cn/20210220153045256.png)

## 1.2 手机屏幕现状

![](https://img-blog.csdnimg.cn/2021022015322696.png)

## 1.3 常见移动端屏幕尺寸

![](https://img-blog.csdnimg.cn/20210220153441903.png)

## 1.4 移动端调试方法

- `Chrome DevTools`（谷歌浏览器）的模拟手机调试
- 搭建本地 `web` 服务器，手机和服务器一个局域网内，通过手机访问服务器
- 使用外网服务器，直接 `IP` 或 `域名` 访问

## 1.5 总结

- 移动端浏览器我们主要对 `webkit` 内核进行兼容
- 我们现在开发的移动端主要针对手机端开发
- 现在移动端碎片化比较严重，分辨率和屏幕尺寸大小不一
- 学会用谷歌浏览器模拟手机界面以及调试

# 二、视口

`视口（viewport）`就是浏览器显示页面内容的屏幕区域，视口可以分为布局视口、视觉视口和理想视口

## 2.1 布局视口 layout viewport

- 一般移动设备的浏览器都默认设置了一个布局视口，用于解决早期的PC端页面在手机上显示的问题
- iOS, Android基本都将这个视口分辨率设置为 980px，所以PC上的网页大多都能在手机上呈现，只不过元素看上去很小，一般默认可以通过手动缩放网页

![](https://img-blog.csdnimg.cn/20210220154103491.png)

## 2.2 视觉视口 visual viewport

- 字面意思，它是用户正在看到的网站的区域，注意：是网站的区域
- 我们可以通过缩放去操作视觉视口，但不会影响布局视口，布局视口仍保持原来的宽度

![](https://img-blog.csdnimg.cn/20210220154103529.png)

## 2.3 理想视口 ideal viewport

- 为了使网站在移动端有最理想的浏览和阅读宽度而设定
- 理想视口，对设备来讲，是最理想的视口尺寸
- 需要手动添写 `meta` 视口标签通知浏览器操作
- `meta` 视口标签的主要目的：布局视口的宽度应该与理想视口的宽度一致，简单理解就是设备有多宽，我们布局的视口就多宽

## 2.4 总结

- 视口就是浏览器显示页面内容的屏幕区域
- 视口分为布局视口、视觉视口和理想视口
- 我们移动端布局想要的是理想视口就是手机屏幕有多宽，我们的布局视口就有多宽
- 想要理想视口，我们需要给我们的移动端页面添加 `meta` 视口标签

## 2.5 meta视口标签

```html
<meta name="viewport" content="width=device-width, user-scalable=no,
initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
```

![](https://img-blog.csdnimg.cn/20210220154645793.png)

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport"
        content="width=device-width, initial-scale=1.0,maximum-scale=1.0, minimum-scale=1.0, user-scalable=no">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>01-meta视口标签</title>
</head>

<body>
    黑马程序员
</body>

</html>
```

## 2.6 标准的viewport设置

- 视口宽度和设备保持一致
- 视口的默认缩放比例 `1.0`
- 不允许用户自行缩放
- 最大允许的缩放比例 `1.0`
- 最小允许的缩放比例 `1.0`

# 三、二倍图

## 3.1 物理像素&物理像素比

- 物理像素点指的是屏幕显示的最小颗粒，是物理真实存在的。这是厂商在出厂时就设置好了,比如 苹果 6\7\8 是 `750 * 1334`
- 我们开发时候的 `1px` 不是一定等于1个物理像素的
- PC端页面，1个px 等于1个物理像素的，但是移动端就不尽相同
- 一个px的能显示的物理像素点的个数，称为物理像素比或屏幕像素比
- PC端 和 早前的手机屏幕 / 普通手机屏幕：`1 CSS像素 = 1 物理像素` 的
- `Retina（视网膜屏幕）`是一种显示技术，可以将把更多的物理像素点压缩至一块屏幕里，从而达到更高的分辨率，并提高屏幕显示的细腻程度

![](https://img-blog.csdnimg.cn/20210220155403361.png)

![](https://img-blog.csdnimg.cn/20210220155403499.png)

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>02-物理像素比</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }

        div {
            width: 300px;
            height: 300px;
            background-color: pink;
        }

        /* 1. 物理像素 就是我们说的分辨率  iPhone8的物理像素是 750 */
        /* 2. 在 iPhone8里面  1px 开发像素  =  2个物理像素  */
    </style>
</head>

<body>
    <div></div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210220180230587.png)

![](https://img-blog.csdnimg.cn/20210220182043182.png)

## 3.2 多倍图

- 对于一张 `50px * 50px` 的图片，在手机 `Retina` 屏中打开，按照刚才的物理像素比会放大倍数，这样会造成图片模糊
- 在标准的 `viewport` 设置中，使用倍图来提高图片质量，解决在高清设备中的模糊问题
- 通常使用二倍图， 因为 `iPhone 6\7\8` 的影响,但是现在还存在 3倍图 4倍图 的情况，这个看实际开发公司需求
- 背景图片 注意缩放问题

```css
/* 在 iphone8 下面 */
img {
	/*原始图片100*100px*/
	width: 50px;
	height: 50px;
}

.box {
	/*原始图片100*100px*/
	background-size: 50px 50px;
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
    <title>03-二倍图做法</title>
    <style>
        /* 我们需要一个50*50像素（css像素）的图片 直接放到我们的iphone8 里面会放大2倍  100* 100 就会模糊 */
        /* 我们采取的是 放一个 100* 100 图片  然后手动的把这个图片 缩小为 50* 50 （css像素） */
        /* 我们准备的图片 比我们实际需要的大小 大2倍，这就方式就是 2倍图 */

        img:nth-child(2) {
            width: 50px;
            height: 50px;
        }
    </style>
</head>

<body>
    <!-- 模糊的 -->
    <img src="images/apple50.jpg" alt="">
    <!-- 我们采取2倍图 -->
    <img src="images/apple100.jpg" alt="">
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210220180557932.png)

![](https://img-blog.csdnimg.cn/20210220182004798.png)

## 3.3 背景缩放 background-size

background-size 属性规定背景图像的尺寸

`background-size: 背景图片宽度 背景图片高度;`

- 单位： `长度|百分比|cover|contain;`
- `cover` 把背景图像扩展至足够大，以使背景图像完全覆盖背景区域
- `contain` 把图像图像扩展至最大尺寸，以使其宽度和高度完全适应内容区域

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>04-背景缩放background-size</title>
    <style>
        div {
            width: 500px;
            height: 500px;
            border: 2px solid red;
            background: url(images/dog.jpg) no-repeat;
            /* background-size: 图片的宽度 图片的高度; */
            /* background-size: 500px 200px; */
            /* 1.只写一个参数 肯定是宽度 高度省略了  会等比例缩放 */
            /* background-size: 500px; */
            /* 2. 里面的单位可以跟%  相对于父盒子来说的 */
            /* background-size: 50%; */
            /* 3. cover 等比例拉伸 要完全覆盖div盒子  可能有部分背景图片显示不全 */
            /* background-size: cover; */
            /* 4. contain 高度和宽度等比例拉伸 当宽度 或者高度 铺满div盒子就不再进行拉伸了 可能有部分空白区域 */
            background-size: contain;
        }
    </style>
</head>

<body>
    <div></div>
    <p></p>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210220180835373.png)

![](https://img-blog.csdnimg.cn/20210220181931144.png)

---

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>05-背景图片2倍图</title>

    <style>
        /* 1. 我们有一个 50 * 50的盒子需要一个背景图片，但是根据分析这个图片还是要准备2倍， 100*100 */
        /* 2. 我们需要把这个图片缩放一半，也就是 50*50  background-size*/

        div {
            width: 50px;
            height: 50px;
            border: 1px solid red;
            background: url(images/apple100.jpg) no-repeat;
            background-size: 50px 50px;
        }
    </style>
</head>

<body>
    <div></div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210220181022803.png)

![](https://img-blog.csdnimg.cn/20210220181850824.png)

## 3.4 多倍图切图 cutterman

- @3X 3倍图
- @2X 2倍图
- @1X 1倍图原图

![](https://img-blog.csdnimg.cn/20210220160110383.png)

# 四、移动端开发选择

## 4.1 移动端主流方案

![](https://img-blog.csdnimg.cn/20210220160358405.png)

## 4.2 单独移动端页面（主流）

通常情况下，网址域名前面加 `m(mobile)` 可以打开移动端，通过判断设备，如果是移动设备打开，则跳到移动端页面

![](https://img-blog.csdnimg.cn/20210220160524112.png)

## 4.3 响应式兼容PC移动端

三星电子官网：[ www.samsung.com/cn/]( www.samsung.com/cn/) ，通过判断屏幕宽度来改变样式，以适应不同终端

缺点：制作麻烦， 需要花很大精力去调兼容性问题

![](https://img-blog.csdnimg.cn/20210220160729432.png)

## 4.4 总结

现在市场常见的移动端开发有 `单独制作移动端页面` 和 `响应式页面` 两种方案，现在市场主流的选择还是 `单独制作移动端页面`

# 五、移动端技术解决方案

## 5.1 移动端浏览器

- 移动端浏览器基本以 `webkit` 内核为主，因此我们就考虑 `webkit` 兼容性问题
- 我们可以放心使用 `H5` 标签 和 `CSS3` 样式
- 同时我们浏览器的私有前缀我们只需要考虑添加 `webkit` 即可

![](https://img-blog.csdnimg.cn/20210220161046257.png)

## 5.2 CSS初始化 normalize.css

移动端 CSS 初始化推荐使用 `normalize.css/`

- Normalize.css：保护了有价值的默认值
- Normalize.css：修复了浏览器的 bug
- Normalize.css：是模块化的
- Normalize.css：拥有详细的文档

官网地址：[http://necolas.github.io/normalize.css/](http://necolas.github.io/normalize.css/) 

## 5.3 CSS3 盒子模型 box-sizing

- 传统模式宽度计算：`盒子的宽度` = CSS中设置的 `width` + `border` + `padding`
- CSS3 盒子模型： 盒子的宽度 = CSS中设置的宽度 `width` 里面包含了 `border` 和 `padding`
  也就是说，我们的 CSS3 中的盒子模型，`padding` 和 `border` 不会撑大盒子了

```css
/*CSS3盒子模型*/
box-sizing: border-box;
/*传统盒子模型*/
box-sizing: content-box;
```

**传统 or CSS3 盒子模型？**

- 移动端可以全部 CSS3 盒子模型
- PC端 如果完全需要兼容，我们就用传统模式，如果不考虑兼容性，我们就选择 CSS3 盒子模型

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>06-CSS3盒子模型</title>
    <style>
        div:nth-child(1) {
            /* 传统盒子模型= width + border + padding */
            width: 200px;
            height: 200px;
            background-color: pink;
            padding: 10px;
            border: 10px solid red;
            box-sizing: content-box;
        }

        div:nth-child(2) {
            /* 有了这句话就让盒子变成CSS3盒子模型 */
            /* padding 和 border 不会再撑大盒子了 */
            box-sizing: border-box;
            width: 200px;
            height: 200px;
            background-color: purple;
            padding: 10px;
            border: 10px solid blue;
        }
    </style>
</head>

<body>
    <div></div>
    <div></div>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210220181218751.png)

![](https://img-blog.csdnimg.cn/20210220181808704.png)

## 5.4 特殊样式

```css
/*CSS3盒子模型*/
box-sizing: border-box;
-webkit-box-sizing: border-box;
/*点击高亮我们需要清除清除 设置为transparent 完成透明*/
-webkit-tap-highlight-color: transparent;
/*在移动端浏览器默认的外观在iOS上加上这个属性才能给按钮和输入框自定义样式*/
-webkit-appearance: none;
/*禁用长按页面时的弹出菜单*/
img,
a { -webkit-touch-callout: none; }
```

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>07-特殊样式</title>
    <style>
        a {
            -webkit-tap-highlight-color: transparent;
        }

        input {
            -webkit-appearance: none;
        }
    </style>
</head>

<body>
    <a href="#">黑马</a>
    <input type="button" value="按钮">
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210220181339661.png)

![](https://img-blog.csdnimg.cn/20210220181723277.png)

# 六、移动端常见布局

**移动端技术选型**

移动端布局和以前我们学习的PC端有所区别：

![](https://img-blog.csdnimg.cn/20210220161742715.png)

## 6.1 流式布局（百分比布局）

- 流式布局，就是百分比布局，也称非固定像素布局
- 通过盒子的宽度设置成百分比来根据屏幕的宽度来进行伸缩，不受固定像素的限制，内容向两侧填充
- 流式布局方式是移动web开发使用的比较常见的布局方式

![](https://img-blog.csdnimg.cn/20210220161914266.png)

- `max-width` 最大宽度 （`max-height` 最大高度）
- `min-width` 最小宽度 （`min-height` 最小高度）

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>08-流式布局</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }

        section {
            width: 100%;
            max-width: 980px;
            min-width: 320px;
            margin: 0 auto;
        }

        section div {
            float: left;
            width: 50%;
            height: 400px;
        }

        section div:nth-child(1) {
            background-color: pink;
        }

        section div:nth-child(2) {
            background-color: purple;
        }
    </style>
</head>

<body>
    <section>
        <div></div>
        <div></div>
    </section>
</body>

</html>
```

![](https://img-blog.csdnimg.cn/20210220181518523.png)

![](https://img-blog.csdnimg.cn/20210220181627107.png)

## 6.2 案例：京东移动端首页

- 访问地址：[m.jd.com](m.jd.com)

![](https://img-blog.csdnimg.cn/2021022016343296.png)

- 1、技术选项

方案：我们采取单独制作移动页面方案

技术：布局采取流式布局

- 2、搭建相关文件夹结构

![](https://img-blog.csdnimg.cn/20210220164715257.png)

- 3、设置视口标签以及引入初始化样式

```html
<meta name="viewport" content="width=device-width, user-scalable=no,
initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
<link rel="stylesheet" href="css/normalize.css">
<link rel="stylesheet" href="css/index.css">
```

- 4、常用初始化样式

```css
body {
	margin: 0 auto;
	min-width: 320px;
	max-width: 640px;
	background: #fff;
	font-size: 14px;
	font-family: -apple-system, Helvetica, sans-serif;
	line-height: 1.5;
	color: #666;
}
```

- 5、二倍精灵图做法

在 `firework` 里面把精灵图等比例缩放为原来的一半

之后根据大小测量坐标

注意代码里面 `background-size` 也要写： 精灵图原来宽度的一半

- 6、图片格式

![](https://img-blog.csdnimg.cn/202102201639533.png)

案例结构及内容：

![](https://img-blog.csdnimg.cn/20210220182424587.png)

![](https://img-blog.csdnimg.cn/20210220182348410.png)

![](https://img-blog.csdnimg.cn/20210220182348417.png)

![](https://img-blog.csdnimg.cn/20210220182348497.png)

- index.html

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport"
        content="width=device-width, initial-scale=1.0, user-scalable=no,maximum-scale=1.0,minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <!-- 引入我们的css初始化文件 -->
    <link rel="stylesheet" href="css/normalize.css">
    <!-- 引入我们首页的css -->
    <link rel="stylesheet" href="css/index.css">
    <title>Document</title>
</head>

<body>
    <!-- 顶部 -->
    <header class="app">
        <ul>
            <li>
                <img src="images/close.png" alt="">
            </li>
            <li>
                <img src="images/logo.png" alt="">
            </li>
            <li>打开京东App，购物更轻松</li>
            <li>立即打开</li>
        </ul>
    </header>
    <!-- 搜索 -->
    <div class="search-wrap">
        <div class="search-btn"></div>
        <div class="search">
            <div class="jd-icon"></div>
            <div class="sou"></div>
        </div>
        <div class="search-login">登陆</div>
    </div>
    <!-- 主体内容部分 -->
    <div class="main-content">
        <!-- 滑动图 -->
        <div class="slider">
            <img src="upload/banner.dpg" alt="">
        </div>

        <!-- 小家电品牌日 -->
        <div class="brand">
            <div>
                <a href="#">
                    <img src="upload/pic11.dpg" alt="">
                </a>
            </div>
            <div>
                <a href="#">
                    <img src="upload/pic22.dpg" alt="">
                </a>

            </div>
            <div>
                <a href="#">
                    <img src="upload/pic33.dpg" alt="">
                </a>

            </div>
        </div>
        <!-- nav部分 -->
        <nav class="clearfix">
            <a href="">
                <img src="upload/nav1.webp" alt="">
                <span>京东超市</span>
            </a>

            <a href="">
                <img src="upload/nav2.webp" alt="">
                <span>京东超市</span>
            </a>

            <a href="">
                <img src="upload/nav1.webp" alt="">
                <span>京东超市</span>
            </a>

            <a href="">
                <img src="upload/nav1.webp" alt="">
                <span>京东超市</span>
            </a>

            <a href="">
                <img src="upload/nav1.webp" alt="">
                <span>京东超市</span>
            </a>

            <a href="">
                <img src="upload/nav3.webp" alt="">
                <span>京东超市</span>
            </a>

            <a href="">
                <img src="upload/nav1.webp" alt="">
                <span>京东超市</span>
            </a>

            <a href="">
                <img src="upload/nav1.webp" alt="">
                <span>京东超市</span>
            </a>

            <a href="">
                <img src="upload/nav1.webp" alt="">
                <span>京东超市</span>
            </a>

            <a href="">
                <img src="upload/nav1.webp" alt="">
                <span>京东超市</span>
            </a>

        </nav>
        <!-- 新闻模块 -->
        <div class="news">
            <a href="#">
                <img src="upload/new1.dpg" alt="">
            </a>
            <a href="#">
                <img src="upload/new2.dpg" alt="">

            </a>
            <a href="#">
                <img src="upload/new3.dpg" alt="">

            </a>
        </div>
    </div>
</body>

</html>
```

- index.css

```css
body {
  width: 100%;
  min-width: 320px;
  max-width: 640px;
  margin: 0 auto;
  font-size: 14px;
  font-family: -apple-system, Helvetica, sans-serif;
  color: #666;
  line-height: 1.5;
}

/*点击高亮我们需要清除清除  设置为transparent 完成透明*/

* {
  -webkit-tap-highlight-color: transparent;
}

/*在移动端浏览器默认的外观在iOS上加上这个属性才能给按钮和输入框自定义样式*/

input {
  -webkit-appearance: none;
}

/*禁用长按页面时的弹出菜单*/

img,
a {
  -webkit-touch-callout: none;
}

a {
  color: #666;
  text-decoration: none;
}

ul {
  margin: 0;
  padding: 0;
  list-style: none;
}

img {
  vertical-align: middle;
}

div {
  /* css3 盒子模型 */
  box-sizing: border-box;
}

.clearfix:after {
  content: "";
  display: block;
  line-height: 0;
  visibility: hidden;
  height: 0;
  clear: both;
}

.app {
  height: 45px;
}

.app ul li {
  float: left;
  height: 45px;
  line-height: 45px;
  background-color: #333333;
  text-align: center;
  color: #fff;
}

.app ul li:nth-child(1) {
  width: 8%;
}

.app ul li:nth-child(1) img {
  width: 10px;
}

.app ul li:nth-child(2) {
  width: 10%;
}

.app ul li:nth-child(2) img {
  width: 30px;
  vertical-align: middle;
}

.app ul li:nth-child(3) {
  width: 57%;
}

.app ul li:nth-child(4) {
  width: 25%;
  background-color: #f63515;
}

/* 搜索 */

.search-wrap {
  position: fixed;
  overflow: hidden;
  width: 100%;
  height: 44px;
  min-width: 320px;
  max-width: 640px;
}

.search-btn {
  position: absolute;
  top: 0;
  left: 0;
  width: 40px;
  height: 44px;
}

.search-btn::before {
  content: "";
  display: block;
  width: 20px;
  height: 18px;
  background: url(../images/s-btn.png) no-repeat;
  background-size: 20px 18px;
  margin: 14px 0 0 15px;
}

.search-login {
  position: absolute;
  right: 0;
  top: 0;
  width: 40px;
  height: 44px;
  color: #fff;
  line-height: 44px;
}

.search {
  position: relative;
  height: 30px;
  background-color: #fff;
  margin: 0 50px;
  border-radius: 15px;
  margin-top: 7px;
}

.jd-icon {
  width: 20px;
  height: 15px;
  position: absolute;
  top: 8px;
  left: 13px;
  background: url(../images/jd.png) no-repeat;
  background-size: 20px 15px;
}

.jd-icon::after {
  content: "";
  position: absolute;
  right: -8px;
  top: 0;
  display: block;
  width: 1px;
  height: 15px;
  background-color: #ccc;
}

.sou {
  position: absolute;
  top: 8px;
  left: 50px;
  width: 18px;
  height: 15px;
  background: url(../images/jd-sprites.png) no-repeat -81px 0;
  background-size: 200px auto;
}

.slider img {
  width: 100%;
}

/* 品牌日 */

.brand {
  overflow: hidden;
  border-radius: 10px 10px 0 0;
}

.brand div {
  float: left;
  width: 33.33%;
}

.brand div img {
  width: 100%;
}

/* nav */

nav {
  padding-top: 5px;
}

nav a {
  float: left;
  width: 20%;
  text-align: center;
}

nav a img {
  width: 40px;
  margin: 10px 0;
}

nav a span {
  display: block;
}

/* news */

.news {
  margin-top: 20px;
}

.news img {
  width: 100%;
}

.news a {
  float: left;
  box-sizing: border-box;
}

.news a:nth-child(1) {
  width: 50%;
}

/* .news a:nth-child(2),
.news a:nth-child(3),
{
    width: 25%;
} */

/* n+2 就是从从2个往后面选 */

.news a:nth-child(n + 2) {
  width: 25%;
  border-left: 1px solid #ccc;
}

/* .news a:nth-child(3) {
    width: 25%;
} */
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

![](https://img-blog.csdnimg.cn/20210220182720574.png)

![](https://img-blog.csdnimg.cn/20210220182718501.png)

# 七、总结

![](https://img-blog.csdnimg.cn/20210220162057212.png)


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
