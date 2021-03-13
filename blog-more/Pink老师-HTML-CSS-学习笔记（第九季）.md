---
title: Pink老师 HTML CSS 学习笔记（第九季）
date: 2021-02-09 17:01:25
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

# Pink老师 HTML CSS 学习笔记（第九季）

# 【学成在线案例】

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Pink老师 HTML CSS 学习笔记（第九季）](#pink%E8%80%81%E5%B8%88-html-css-%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%E7%AC%AC%E4%B9%9D%E5%AD%A3)
- [【学成在线案例】](#%E5%AD%A6%E6%88%90%E5%9C%A8%E7%BA%BF%E6%A1%88%E4%BE%8B)
- [一、准备素材和工具](#%E4%B8%80%E5%87%86%E5%A4%87%E7%B4%A0%E6%9D%90%E5%92%8C%E5%B7%A5%E5%85%B7)
- [二、案例准备工作](#%E4%BA%8C%E6%A1%88%E4%BE%8B%E5%87%86%E5%A4%87%E5%B7%A5%E4%BD%9C)
- [三、CSS 属性书写顺序(重点)](#%E4%B8%89css-%E5%B1%9E%E6%80%A7%E4%B9%A6%E5%86%99%E9%A1%BA%E5%BA%8F%E9%87%8D%E7%82%B9)
- [四、页面布局分析](#%E5%9B%9B%E9%A1%B5%E9%9D%A2%E5%B8%83%E5%B1%80%E5%88%86%E6%9E%90)
- [五、确定版心](#%E4%BA%94%E7%A1%AE%E5%AE%9A%E7%89%88%E5%BF%83)
- [六、头部制作](#%E5%85%AD%E5%A4%B4%E9%83%A8%E5%88%B6%E4%BD%9C)
- [七、banner 制作](#%E4%B8%83banner-%E5%88%B6%E4%BD%9C)
- [八、精品推荐小模块](#%E5%85%AB%E7%B2%BE%E5%93%81%E6%8E%A8%E8%8D%90%E5%B0%8F%E6%A8%A1%E5%9D%97)
- [九、精品推荐大模块](#%E4%B9%9D%E7%B2%BE%E5%93%81%E6%8E%A8%E8%8D%90%E5%A4%A7%E6%A8%A1%E5%9D%97)
- [十、底部模块](#%E5%8D%81%E5%BA%95%E9%83%A8%E6%A8%A1%E5%9D%97)
- [十一、代码](#%E5%8D%81%E4%B8%80%E4%BB%A3%E7%A0%81)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

![](https://img-blog.csdnimg.cn/20210209182304293.png)

# 一、准备素材和工具

- 1、学成在线 `PSD` 源文件

- 2、开发工具 = `PS`（切图）+ `VSCode`（代码）+ `Chrome`（测试）

# 二、案例准备工作

**我们本次采取结构与样式相分离思想：**

- 1、创建 `study` 目录文件夹 (用于存放我们这个页面的相关内容)。
- 2、`study` 目录内新建 `images` 文件夹，用于保存图片。
- 3、新建首页文件 `index.html`（以后我们的网站首页统一规定为 `index.html` )。
- 4、新建 `style.css` 样式文件。我们本次采用外链样式表。
- 5、将样式引入到我们的 `HTML` 页面文件中。
- 6、样式表写入清除内外边距的样式，来检测样式表是否引入成功。

# 三、CSS 属性书写顺序(重点)

**建议遵循以下顺序：**

- 1、布局定位属性：`display / position / float / clear / visibility / overflow`（建议 `display` 第一个写，毕竟关系到模式）
- 2、自身属性：`width / height / margin / padding / border / background`
- 3、文本属性：`color / font / text-decoration / text-align / vertical-align / white- space / break-word`
- 4、其他属性（CSS3）：`content / cursor / border-radius / box-shadow / text-shadow / background:linear-gradient …`

```css
.jdc {
	display: block;
	position: relative;
	float: left;
	width: 100px;
	height: 100px;
	margin: 0 10px;
	padding: 20px 0;
	font-family: Arial, 'Helvetica Neue', Helvetica, sans-serif;
	color: #333;
	background: rgba(0,0,0,.5);
	border-radius: 10px;
}
```

# 四、页面布局分析

**为了提高网页制作的效率，布局时通常有以下的布局流程：**

- 1、必须确定页面的版心（可视区），我们测量可得知。
- 2、分析页面中的行模块，以及每个行模块中的列模块。其实页面布局，就是一行行罗列而成的。
- 3、制作 `HTML` 结构。我们还是遵循，先有结构，后有样式的原则。结构永远最重要。
- 4、开始运用盒子模型的原理，通过 `DIV+CSS` 布局来控制网页的各个模块。

# 五、确定版心

**这个页面的版心是 1200 像素，每个版心都要水平居中对齐，可以定义版心为公共类：**

```css
.w {
	width: 1200px;
	margin: auto;
}
```

# 六、头部制作

![](https://img-blog.csdnimg.cn/20210209182301961.png)

- 1 号是版心盒子 `header` `1200 * 42` 的盒子水平居中对齐，上下给一个 `margin` 值就可以
- 版心盒子里面包含 2 号盒子 `logo`
- 版心盒子里面包含 3 号盒子 `nav` 导航栏
- 版心盒子里面包含 4 号盒子 `search` 搜索框
- 版心盒子里面包含 5 号盒子 `user` 个人信息
- 注意：要求里面的 4 个盒子必须都是浮动

# 七、banner 制作

![](https://img-blog.csdnimg.cn/20210209182303406.png)

- 1 号盒子是通栏的大盒子 `banner`，不给宽度，给高度，给一个蓝色背景
- 2 号盒子是版心，要水平居中对齐
- 3 号盒子版心内，左对齐 `subnav` 侧导航栏
- 4 号盒子版心内，右对齐 `course` 课程

# 八、精品推荐小模块

![](https://img-blog.csdnimg.cn/20210209182512463.png)

- 大盒子水平居中 `goods` 精品，注意此处有个盒子阴影
- 1 号盒子是标题 `H3` 左侧浮动
- 2 号盒子里面放链接左侧浮动， `goods-item` 距离可以控制链接的左右外边距（注意行内元素只给左右内外边距）
- 3 号盒子右浮动 `mod` 修改

# 九、精品推荐大模块

![](https://img-blog.csdnimg.cn/2021020918230473.png)

- 1 号盒子为最大的盒子， `box` 版心水平居中对齐
- 2 号盒子为上面部分，`box-hd --` 里面左侧标题 `H3` 左浮动，右侧链接 `a` 右浮动
- 3 号盒子为底下部分，`box-bd --` 里面是无序列表，有 10 个小 `li` 组成
- 小 `li` 外边距的问题，这里有个小技巧：给 `box-hd` 宽度为 `1215` 就可以一行装开 `5` 个 `li`

复习点：我们用到清除浮动，因为 `box-hd` 里面的盒子个数不一定是多少，所以我们就不给高度了，但是里面的盒子浮动会影响下面的布局，因此需要清除浮动。

# 十、底部模块

![](https://img-blog.csdnimg.cn/20210209182302118.png)

- 1 号盒子是通栏大盒子，底部 `footer` 给高度，底色是白色
- 2 号盒子版心水平居中
- 3 号盒子版权 `copyright` 左对齐
- 4 号盒子链接组 `links` 右对齐

# 十一、代码

- `index.html`

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>学车在线首页</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>

    <!-- 1.头部区域开始啦！ -->
    <div class="header w">

        <!-- logo 部分 -->
        <div class="logo">
            <img src="images/logo.png" alt="">
        </div>

        <!-- 导航栏部分 nav -->
        <div class="nav">
            <!-- 对于大量的链接堆叠来说：一定要将 a 放在列表中，这将能大大提高 SEO，
                因为浏览器会将有大量链接堆叠的情况视为恶意增加链接，会自动将其降低排名， -->
            <ul>
                <li><a href="#">首页</a></li>
                <li><a href="#">课程</a></li>
                <li><a href="#">职业规划</a></li>
            </ul>
        </div>

        <!-- 搜索模块 -->
        <!-- 在实际开发中，搜索框不用 text 而是用 search，search 会自带按钮所以也不用再加 button -->
        <div class="search">
            <input type="text" value="输入关键词">
            <button></button>
        </div>

        <!-- 用户模块 -->
        <div class="user">
            <!-- 此处，头像及名称直接丢到 div 中即可，两者之间有一个空格 -->
            <img src="images/user.png" alt=""> qq-leishui
        </div>
    </div>
    <!-- 头部区域结束啦！ -->
    <!---->
    <!---->
    <!---->
    <!-- 2. banner 部分开始啦！ -->
    <div class="banner">

        <!-- 版心 -->
        <div class="w">

            <!-- 侧导航栏 -->
            <div class="subnav">
                <ul>
                    <li><a href="#">前端开发 <span> &gt; </span> </a></li>
                    <li><a href="#">前端开发 <span> &gt; </span> </a></li>
                    <li><a href="#">前端开发 <span> &gt; </span> </a></li>
                    <li><a href="#">前端开发 <span> &gt; </span> </a></li>
                    <li><a href="#">前端开发 <span> &gt; </span> </a></li>
                    <li><a href="#">前端开发 <span> &gt; </span> </a></li>
                    <li><a href="#">前端开发 <span> &gt; </span> </a></li>
                    <li><a href="#">前端开发 <span> &gt; </span> </a></li>
                    <li><a href="#">前端开发 <span> &gt; </span> </a></li>
                </ul>
            </div>

            <!-- course 课程表模块 -->
            <div class="course">
                <!-- 对于标题性质的文字优先使用 h 便签 -->
                <!-- 对于标题下的文段内容优先使用 p 标签 -->
                <h2>我的课程表</h2>
                <!-- hd 指上面部分，bd 指下面部分 -->
                <div class="bd">
                    <ul>
                        <li>
                            <h4>继续学习 程序语言设计</h4>
                            <p>正在学习-使用对象</p>
                        </li>
                        <li>
                            <h4>继续学习 程序语言设计</h4>
                            <p>正在学习-使用对象</p>
                        </li>
                        <li>
                            <h4>继续学习 程序语言设计</h4>
                            <p>正在学习-使用对象</p>
                        </li>
                    </ul>

                    <!-- 有关展开栏，详细页用 more 修饰 -->
                    <a href="#" class="more">全部课程</a>
                </div>
            </div>
        </div>
    </div>
    <!-- banner 部分结束啦！ -->
    <!---->
    <!---->
    <!---->
    <!-- 3.精品推荐模块开始啦！ -->
    <div class="goods w">

        <h3>精品推荐</h3>
        <ul>
            <li><a href="#">jQuery</a></li>
            <li><a href="#">jQuery</a></li>
            <li><a href="#">jQuery</a></li>
            <li><a href="#">jQuery</a></li>
            <li><a href="#">jQuery</a></li>
        </ul>

        <a href="#" class="mod">修改兴趣</a>
    </div>
    <!-- 精品推荐模块结束啦！ -->
    <!---->
    <!---->
    <!---->
    <!-- 4. box 核心内容区域开始啦！ -->
    <div class="box w">

        <div class="box-hd">
            <h3>精品推荐</h3>
            <a href="#">查看全部</a>
        </div>

        <div class="box-bd">
            <ul class="clearfix">
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>
                        Think PHP 5.0 博客系统实战项目演练
                    </h4>
                    <div class="info">
                        <span>高级</span> • 1125人在学习
                    </div>
                </li>
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>
                        Think PHP 5.0 博客系统实战项目演练
                    </h4>
                    <div class="info">
                        <span>高级</span> • 1125人在学习
                    </div>
                </li>
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>
                        Think PHP 5.0 博客系统实战项目演练
                    </h4>
                    <div class="info">
                        <span>高级</span> • 1125人在学习
                    </div>
                </li>
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>
                        Think PHP 5.0 博客系统实战项目演练
                    </h4>
                    <div class="info">
                        <span>高级</span> • 1125人在学习
                    </div>
                </li>
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>
                        Think PHP 5.0 博客系统实战项目演练
                    </h4>
                    <div class="info">
                        <span>高级</span> • 1125人在学习
                    </div>
                </li>
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>
                        Think PHP 5.0 博客系统实战项目演练
                    </h4>
                    <div class="info">
                        <span>高级</span> • 1125人在学习
                    </div>
                </li>
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>
                        Think PHP 5.0 博客系统实战项目演练
                    </h4>
                    <div class="info">
                        <span>高级</span> • 1125人在学习
                    </div>
                </li>
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>
                        Think PHP 5.0 博客系统实战项目演练
                    </h4>
                    <div class="info">
                        <span>高级</span> • 1125人在学习
                    </div>
                </li>
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>
                        Think PHP 5.0 博客系统实战项目演练
                    </h4>
                    <div class="info">
                        <span>高级</span> • 1125人在学习
                    </div>
                </li>
                <li>
                    <img src="images/pic.png" alt="">
                    <h4>
                        Think PHP 5.0 博客系统实战项目演练
                    </h4>
                    <div class="info">
                        <span>高级</span> • 1125人在学习
                    </div>
                </li>
            </ul>
        </div>
    </div>
    <!-- 4. box核心内容区域结束啦！ -->
    <!---->
    <!---->
    <!---->
    <!-- 5. footer 模块制作开始啦！ -->
    <div class="footer">

        <!-- 版心 -->
        <div class="w">

            <div class="copyright">
                <img src="images/logo.png" alt="">
                <p>学成在线致力于普及中国最好的教育它与中国一流大学和机构合作提供在线课程。<br> © 2017年XTCG Inc.保留所有权利。-沪ICP备15025210号</p>
                <a href="#" class="app">下载APP</a>
            </div>

            <div class="links">
                <dl>
                    <dt>关于学成网</dt>
                    <dd><a href="#">关于</a></dd>
                    <dd><a href="#">管理团队</a></dd>
                    <dd><a href="#">工作机会</a></dd>
                    <dd><a href="#">客户服务</a></dd>
                    <dd><a href="#">帮助</a></dd>
                </dl>
                <dl>
                    <dt>关于学成网</dt>
                    <dd><a href="#">关于</a></dd>
                    <dd><a href="#">管理团队</a></dd>
                    <dd><a href="#">工作机会</a></dd>
                    <dd><a href="#">客户服务</a></dd>
                    <dd><a href="#">帮助</a></dd>
                </dl>
                <dl>
                    <dt>关于学成网</dt>
                    <dd><a href="#">关于</a></dd>
                    <dd><a href="#">管理团队</a></dd>
                    <dd><a href="#">工作机会</a></dd>
                    <dd><a href="#">客户服务</a></dd>
                    <dd><a href="#">帮助</a></dd>
                </dl>
            </div>
        </div>
    </div>
</body>

</html>
```

- `style.css`

```css
/* 将页面所有的内外边距置零 */

* {
    margin: 0;
    padding: 0;
}


/* 设置版心大小，居中放置 */

.w {
    width: 1200px;
    margin: auto;
}


/* 设置页面背景颜色 */

body {
    background-color: #f3f5f7;
}


/* 除去所有 li 前的 符号 */

li {
    list-style: none;
}


/* 除去所有链接的样式 */

a {
    text-decoration: none;
}


/* 双伪元素清除浮动 */

.clearfix:before,
.clearfix:after {
    content: "";
    display: table;
}

.clearfix:after {
    clear: both;
}

.clearfix {
    *zoom: 1;
}

.header {
    height: 42px;
    /* background-color: pink; */
    /* 注意此地方会层叠 w 里面的 margin */
    /* 让 div 居中 */
    margin: 30px auto;
}

.logo {
    float: left;
    width: 198px;
    height: 42px;
}

.nav {
    float: left;
    margin-left: 60px;
}

.nav ul li {
    float: left;
    margin: 0 15px;
}

.nav ul li a {
    /* a 行内元素转为块元素 */
    display: block;
    height: 42px;
    padding: 0 10px;
    /* 让行高等于盒子的高度，实现居中效果 */
    line-height: 42px;
    font-size: 18px;
    color: #050505;
}


/* 鼠标停留时改变样式 */

.nav ul li a:hover {
    border-bottom: 2px solid #00a4ff;
    color: #00a4ff;
}


/* search搜索模块 */

.search {
    float: left;
    width: 412px;
    height: 42px;
    margin-left: 70px;
}

.search input {
    float: left;
    width: 345px;
    height: 40px;
    border: 1px solid #00a4ff;
    /* 右边框单独设置为 0 */
    border-right: 0;
    color: #bfbfbf;
    font-size: 14px;
    /* 设置一定的内边距，可以使默认文字实现缩进效果 */
    padding-left: 15px;
}

.search button {
    float: left;
    width: 50px;
    height: 42px;
    /* 按钮 button 默认有个边框需要我们手动去掉 */
    border: 0;
    /* 非带链接图片建议都采用背景图片设置，而非 img 标签 */
    background: url(images/btn.png);
}

.user {
    float: right;
    line-height: 42px;
    margin-right: 30px;
    font-size: 14px;
    color: #666;
}


/* banner 区域 */

.banner {
    height: 421px;
    background-color: #1c036c;
}


/* 设置版心区域的大盒子 */

.banner .w {
    height: 421px;
    /* 实际上，此处的大轮播图是一个图片链接要用 img 标签来做，但是这里占时简化了 */
    background: url(images/banner2.png) no-repeat top center;
}


/* 侧边导航栏 */

.subnav {
    /* 左浮动 */
    float: left;
    width: 190px;
    height: 421px;
    /* 半透明背景 */
    background: rgba(0, 0, 0, 0.3);
}


/* 由于 li 是块元素，所以单独占一行，此处刚好合适，不用转换 */

.subnav ul li {
    height: 45px;
    line-height: 45px;
    padding: 0 20px;
}

.subnav ul li a {
    font-size: 14px;
    color: #fff;
}

.subnav ul li a span {
    /* 右浮动 */
    float: right;
}

.subnav ul li a:hover {
    color: #00a4ff;
}


/* 右侧课程信息栏 */

.course {
    /* 右浮动 */
    float: right;
    width: 230px;
    height: 300px;
    background-color: #fff;
    /* 浮动的盒子不会有外边距合并的问题 */
    /* 浮动的盒子不会有外边距合并的问题 */
    /* 浮动的盒子不会有外边距合并的问题 */
    /* 重要的问题说三遍！！！ */
    margin-top: 50px;
}

.course h2 {
    height: 48px;
    background-color: #9bceea;
    text-align: center;
    line-height: 48px;
    font-size: 18px;
    color: #fff;
}

.bd {
    padding: 0 20px;
}

.bd ul li {
    padding: 14px 0;
    border-bottom: 1px solid #ccc;
}

.bd ul li h4 {
    font-size: 16px;
    color: #4e4e4e;
}

.bd ul li p {
    font-size: 12px;
    color: #a5a5a5;
}

.bd .more {
    /* 将 a 转化为块元素独占一行 */
    display: block;
    height: 38px;
    border: 1px solid #00a4ff;
    margin-top: 5px;
    text-align: center;
    line-height: 38px;
    color: #00a4ff;
    font-size: 16px;
    font-weight: 700;
}


/* 精品推荐模块 */

.goods {
    height: 60px;
    background-color: #fff;
    margin-top: 10px;
    box-shadow: 0 2px 3px 3px rgba(0, 0, 0, 0.1);
    /* 行高会继承，会继承给3个孩子 */
    line-height: 60px;
}

.goods h3 {
    float: left;
    margin-left: 30px;
    font-size: 16px;
    color: #00a4ff;
}

.goods ul {
    float: left;
    margin-left: 30px;
}

.goods ul li {
    float: left;
}

.goods ul li a {
    padding: 0 30px;
    font-size: 16px;
    color: #050505;
    border-left: 1px solid #ccc;
}

.mod {
    float: right;
    margin-right: 30px;
    font-size: 14px;
    color: #00a4ff;
}


/* box 核心内容区域 */

.box {
    margin-top: 30px;
}

.box-hd {
    height: 45px;
}

.box-hd h3 {
    float: left;
    font-size: 20px;
    color: #494949;
}

.box-hd a {
    float: right;
    font-size: 12px;
    color: #a5a5a5;
    margin-top: 10px;
    margin-right: 30px;
}


/* 把 li 的父亲 ul 修改的足够宽，一行能装开 5 个盒子就不会换行了 */

.box-bd ul {
    width: 1225px;
}

.box-bd ul li {
    float: left;
    width: 228px;
    height: 270px;
    background-color: #fff;
    margin-right: 15px;
    margin-bottom: 15px;
}

.box-bd ul li img {
    /* 与父亲 li 一样宽 */
    width: 100%;
}

.box-bd ul li h4 {
    margin: 20px 20px 20px 25px;
    font-size: 14px;
    color: #050505;
    font-weight: 400;
}

.box-bd .info {
    margin: 0 20px 0 25px;
    font-size: 12px;
    color: #999;
}

.box-bd .info span {
    color: #ff7c2d;
}


/* footer 模块 */

.footer {
    height: 415px;
    background-color: #fff;
}

.footer .w {
    padding-top: 35px;
}

.copyright {
    float: left;
}

.copyright p {
    font-size: 12px;
    color: #666;
    margin: 20px 0 15px 0;
}

.copyright .app {
    display: block;
    width: 118px;
    height: 33px;
    border: 1px solid #00a4ff;
    text-align: center;
    line-height: 33px;
    color: #00a4ff;
    font-size: 16px;
}

.links {
    float: right;
}

.links dl {
    float: left;
    margin-left: 100px;
}

.links dl dt {
    font-size: 16px;
    color: #333;
    margin-bottom: 5px;
}

.links dl dd a {
    color: #333;
    font-size: 12px;
}
```

- 效果图

![](https://img-blog.csdnimg.cn/2021020921362652.png)

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