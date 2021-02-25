---
title: 零基础自制 博客园 “Mac&ios 黑暗” 主题 制作详解 - 精简归纳
date: 2020-08-29 00:00:00
categories: 
- [个人教程]
tags:
- 博客园
- 主题
- Mac&ios
---
![PC](https://img-blog.csdnimg.cn/20200829143516181.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
<!--more-->
# 零基础自制 博客园 “Mac&ios 黑暗” 主题 制作详解 - 精简归纳

> 原创内容，转载请注明出处！


<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [零基础自制 博客园 “Mac&ios 黑暗” 主题 制作详解 - 精简归纳](#%E9%9B%B6%E5%9F%BA%E7%A1%80%E8%87%AA%E5%88%B6-%E5%8D%9A%E5%AE%A2%E5%9B%AD-macios-%E9%BB%91%E6%9A%97-%E4%B8%BB%E9%A2%98-%E5%88%B6%E4%BD%9C%E8%AF%A6%E8%A7%A3---%E7%B2%BE%E7%AE%80%E5%BD%92%E7%BA%B3)
- [一、简单说明（零基础、超详细）](#%E4%B8%80%E7%AE%80%E5%8D%95%E8%AF%B4%E6%98%8E%E9%9B%B6%E5%9F%BA%E7%A1%80%E8%B6%85%E8%AF%A6%E7%BB%86)
  - [(1)、为什么要写这篇博客？](#1%E4%B8%BA%E4%BB%80%E4%B9%88%E8%A6%81%E5%86%99%E8%BF%99%E7%AF%87%E5%8D%9A%E5%AE%A2)
  - [(2)、博客园如何零基础定制自己的主题？](#2%E5%8D%9A%E5%AE%A2%E5%9B%AD%E5%A6%82%E4%BD%95%E9%9B%B6%E5%9F%BA%E7%A1%80%E5%AE%9A%E5%88%B6%E8%87%AA%E5%B7%B1%E7%9A%84%E4%B8%BB%E9%A2%98)
    - [<1>、进入自己的博客主页点击管理](#1%E8%BF%9B%E5%85%A5%E8%87%AA%E5%B7%B1%E7%9A%84%E5%8D%9A%E5%AE%A2%E4%B8%BB%E9%A1%B5%E7%82%B9%E5%87%BB%E7%AE%A1%E7%90%86)
    - [<2>、点击设置](#2%E7%82%B9%E5%87%BB%E8%AE%BE%E7%BD%AE)
    - [<3>、当前页面下滑找到博客皮肤及定制 CSS](#3%E5%BD%93%E5%89%8D%E9%A1%B5%E9%9D%A2%E4%B8%8B%E6%BB%91%E6%89%BE%E5%88%B0%E5%8D%9A%E5%AE%A2%E7%9A%AE%E8%82%A4%E5%8F%8A%E5%AE%9A%E5%88%B6-css)
    - [<4>、选择一个博客皮肤模板，并写入要替换的 CSS 样式](#4%E9%80%89%E6%8B%A9%E4%B8%80%E4%B8%AA%E5%8D%9A%E5%AE%A2%E7%9A%AE%E8%82%A4%E6%A8%A1%E6%9D%BF%E5%B9%B6%E5%86%99%E5%85%A5%E8%A6%81%E6%9B%BF%E6%8D%A2%E7%9A%84-css-%E6%A0%B7%E5%BC%8F)
    - [<5>、保存设置](#5%E4%BF%9D%E5%AD%98%E8%AE%BE%E7%BD%AE)
- [二、运用举例](#%E4%BA%8C%E8%BF%90%E7%94%A8%E4%B8%BE%E4%BE%8B)
  - [(1)、修改字体颜色](#1%E4%BF%AE%E6%94%B9%E5%AD%97%E4%BD%93%E9%A2%9C%E8%89%B2)
    - [<1>、点击左上角检查元素按钮](#1%E7%82%B9%E5%87%BB%E5%B7%A6%E4%B8%8A%E8%A7%92%E6%A3%80%E6%9F%A5%E5%85%83%E7%B4%A0%E6%8C%89%E9%92%AE)
    - [<2>、鼠标点击标题文字](#2%E9%BC%A0%E6%A0%87%E7%82%B9%E5%87%BB%E6%A0%87%E9%A2%98%E6%96%87%E5%AD%97)
    - [<3>、此时右下角自动定位到标题文字的 CSS 样式](#3%E6%AD%A4%E6%97%B6%E5%8F%B3%E4%B8%8B%E8%A7%92%E8%87%AA%E5%8A%A8%E5%AE%9A%E4%BD%8D%E5%88%B0%E6%A0%87%E9%A2%98%E6%96%87%E5%AD%97%E7%9A%84-css-%E6%A0%B7%E5%BC%8F)
    - [<4>、找到控制标题文字的 CSS 代码段点击颜色并更改颜色](#4%E6%89%BE%E5%88%B0%E6%8E%A7%E5%88%B6%E6%A0%87%E9%A2%98%E6%96%87%E5%AD%97%E7%9A%84-css-%E4%BB%A3%E7%A0%81%E6%AE%B5%E7%82%B9%E5%87%BB%E9%A2%9C%E8%89%B2%E5%B9%B6%E6%9B%B4%E6%94%B9%E9%A2%9C%E8%89%B2)
    - [<5>、复制控制颜色的那一段 CSS 代码段](#5%E5%A4%8D%E5%88%B6%E6%8E%A7%E5%88%B6%E9%A2%9C%E8%89%B2%E7%9A%84%E9%82%A3%E4%B8%80%E6%AE%B5-css-%E4%BB%A3%E7%A0%81%E6%AE%B5)
    - [<6>、粘贴 CSS 样式](#6%E7%B2%98%E8%B4%B4-css-%E6%A0%B7%E5%BC%8F)
  - [(2)、修改字体大小](#2%E4%BF%AE%E6%94%B9%E5%AD%97%E4%BD%93%E5%A4%A7%E5%B0%8F)
  - [(3)、修改字体位置](#3%E4%BF%AE%E6%94%B9%E5%AD%97%E4%BD%93%E4%BD%8D%E7%BD%AE)
- [三、“Mac & ios 黑暗” 定制步骤](#%E4%B8%89mac--ios-%E9%BB%91%E6%9A%97-%E5%AE%9A%E5%88%B6%E6%AD%A5%E9%AA%A4)
  - [(1)、切换 SimpleMemory 主题](#1%E5%88%87%E6%8D%A2-simplememory-%E4%B8%BB%E9%A2%98)
  - [(2)、复制粘贴 CSS 样式](#2%E5%A4%8D%E5%88%B6%E7%B2%98%E8%B4%B4-css-%E6%A0%B7%E5%BC%8F)
  - [(3)、最终效果](#3%E6%9C%80%E7%BB%88%E6%95%88%E6%9E%9C)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# 一、简单说明（零基础、超详细）

## (1)、为什么要写这篇博客？

昨天我写了一篇[《零基础自制 博客园 “赛博朋克” 主题 制作详解 - 精简归纳》](https://www.cnblogs.com/JERRY-Z-J-R/p/13577558.html)的博客发布到博客园首页后很快内便得到了600+的阅读量，当天晚上我在博客中加入了一个统计访问量及访问地的小工具，通过IP访问记录所示：中国香港、美国、印度、马来西亚、新加坡、土耳其，都有IP访问过我的这篇博客！（当时博客已经不在博客园首页了，所以流量高峰期并没有被记录，不然应该会有更多的IP访问被记录）这对我非常的鼓舞，非常开心！！！所以今天我再次写一篇名为：《零基础自制 博客园 ”Mac & ios 黑暗“ 主题 制作详解 - 精简归纳》的主题，希望大家喜欢！！！

<img src="https://img-blog.csdnimg.cn/20200829195020271.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k" width="28%"><img src="https://img-blog.csdnimg.cn/20200829195020318.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k" width="30%"><img src="https://img-blog.csdnimg.cn/20200829195020326.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k" width="36%">



先给大家看一下我上一篇博客主页界面 (“赛博朋克” 风格）：

PC端：

![PC](https://img-blog.csdnimg.cn/20200828134621338.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

移动端：
<img src="https://img-blog.csdnimg.cn/20200829173944486.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k" width="40%">

这是这次的 (“Mac & ios 黑暗” 风格)：

PC端：

![PC](https://img-blog.csdnimg.cn/20200829144045546.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


移动端： 
<img src="https://img-blog.csdnimg.cn/2020082917365660.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k" width="40%">


> 写博客很费精力，转载的话，请注明一下出处！

## (2)、博客园如何零基础定制自己的主题？
> 由于零基础不懂任何前端的网页开发技术，所以这里只是在博客园所提供的主题基础上修改 CSS 样式，从而制定自己的风格，当然，不要看只是修改样式，只要你厉害是可以弄出非常漂亮的效果哦！！！


博客园修改 CSS 样式详细步骤：
### <1>、进入自己的博客主页点击管理
<img src="https://img-blog.csdnimg.cn/20200828135710951.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k" width="66%">

### <2>、点击设置
<img src="https://img-blog.csdnimg.cn/20200828135739926.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k" width="66%">

### <3>、当前页面下滑找到博客皮肤及定制 CSS

<img src="https://img-blog.csdnimg.cn/20200828135829326.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k" width="66%">

### <4>、选择一个博客皮肤模板，并写入要替换的 CSS 样式
### <5>、保存设置


---

# 二、运用举例
> 下文以 SimpleMemory 模板为例

SimpleMemory 默认如下：

![SimpleMemory](https://img-blog.csdnimg.cn/20200828140514951.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
在浏览器中按 F12 键（某些键盘为：Fn + F12）
便可打开博客页面的 HTML CSS 代码

![F12](https://img-blog.csdnimg.cn/20200828140936241.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)



## (1)、修改字体颜色
假如我要把标题改为粉红色
### <1>、点击左上角检查元素按钮
![检查元素](https://img-blog.csdnimg.cn/20200828141220914.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
### <2>、鼠标点击标题文字
![标题文字](https://img-blog.csdnimg.cn/20200828141711265.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
### <3>、此时右下角自动定位到标题文字的 CSS 样式
![标题CSS样式](https://img-blog.csdnimg.cn/20200828141812113.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
### <4>、找到控制标题文字的 CSS 代码段点击颜色并更改颜色
> 如果不知道具体是哪一个，可以一个一个试一下

![更改颜色](https://img-blog.csdnimg.cn/20200828142052885.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

此时页面上的标题颜色已经变成粉红色了，但此时还没有结束，这里只是预览效果，还没有真正改变
### <5>、复制控制颜色的那一段 CSS 代码段
![复制 CSS](https://img-blog.csdnimg.cn/20200828142429762.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
### <6>、粘贴 CSS 样式
![粘贴 CSS 样式](https://img-blog.csdnimg.cn/20200828142802285.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
此时博客页面的颜色便定制为粉红色了！！！

## (2)、修改字体大小
假如我要把标题放大
基本步骤与更改颜色一样，不同的是这里不是修改颜色而是更改或重设字体大小
再次找到刚才标题的 CSS 代码块
添加 font-size:
> 假如本来就有 font-size: 那么只需要修改值即可


<img src="https://img-blog.csdnimg.cn/20200828143318222.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k" width="50%">

选择一个合适的大小，然后复制粘贴到 CSS 设置框中去
完成后的效果：

![字体放大效果](https://img-blog.csdnimg.cn/20200828143524208.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


## (3)、修改字体位置
假如我要把标题居中
基本步骤与更改颜色一样，不同的是这里不是修改颜色而是更改或重设字体在样式框中的位置
这次不是点击标题文字，而是点击标题文字所在样式框

![标题框](https://img-blog.csdnimg.cn/20200828144132644.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
左下角同样出现了标题框样式的 CSS 代码段
添加 text-align:
这里选择居中
> 当然，如果原本就有 text-align: 就只有修改值便可以了

![font-size:](https://img-blog.csdnimg.cn/20200828144220552.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
同样把代码段复制粘贴到 CSS 修改框中

<img src="https://img-blog.csdnimg.cn/20200828144358137.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k" width="50%">

保存后，最终效果：

![最终效果](https://img-blog.csdnimg.cn/20200828144427236.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
其他还有许多可定制的地方，但基本原理相同……

---

# 三、“Mac & ios 黑暗” 定制步骤

## (1)、切换 SimpleMemory 主题

<img src="https://img-blog.csdnimg.cn/20200829143138545.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k" width="50%">


## (2)、复制粘贴 CSS 样式
> 转载请注明出处！！！不可用作商业用途！！！

```css
/*
 * @Author: JEYYR_Z.  SimpleMemory
 * @Date: 2020-08-29 13:40:27
 * @LastEditTime: 2020-08-29 13:44:41
 * @LastEditors: Please set LastEditors
 * @Description: 转载请注明出处！！！不可用作商业用途！！！
 * @FilePath: \undefinede:\MyCode\MyBlog\JERRY'S 教程大本营\零基础自制 博客园 ”暗夜极简“ 主题 10分钟详解 - 精简归纳\新建文本文档.css
 */
body {
    color: #fff;
    background-color: #000;
}
#home {
    background-color: #000;
}
#blogTitle h1 a {
    color: #ffffff;
    font-size: xxx-large;
}
.postTitle a:link, .postTitle a:visited, .postTitle a:active {
    color: #a3e2ff;
    transition: all .4s linear 0s;
}
.postDesc a:link, .postDesc a:visited, .postDesc a:active {
    color: #ff1493;
}
.postDesc {
    color: #b7b7b7;
}
#sideBar a {
    color: #ffffff;
}
#navList a:link, #navList a:visited, #navList a:active {
    color: #e6e6e6;
}
.newsItem, .catListEssay, .catListLink, .catListNoteBook, .catListTag, .catListPostCategory, .catListPostArchive, .catListImageCategory, .catListArticleArchive, .catListView, .catListFeedback, .mySearch, .catListComment, .catListBlogRank, .catList, .catListArticleCategory {
    background: #000;
}
.postBody {
    color: #fff;
    line-height: 1.7;
    font-size: 14px;
}
.postBody blockquote {
    background: url(images/comment.gif) no-repeat 25px 0;
    min-height: 35px;
    _height: 35px;
    line-height: 1.6em;
    color: #fff;
}
a:link {
    color: #fff;
}
.postBody h4 {
    color: #fff;
}
a:visited {
    color: #ff1493;
}
```

## (3)、最终效果
PC端:

![PC](https://img-blog.csdnimg.cn/20200829143516181.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
移动端：
<img src="https://img-blog.csdnimg.cn/20200829173447665.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k" width="40%">

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