---
title: Pink老师 HTML CSS 学习笔记（第四季）
date: 2021-01-21 00:20:34
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

# Pink老师 HTML CSS 学习笔记（第四季）

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Pink老师 HTML CSS 学习笔记（第四季）](#pink%E8%80%81%E5%B8%88-html-css-%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0%E7%AC%AC%E5%9B%9B%E5%AD%A3)
- [Emmet 语法](#emmet-%E8%AF%AD%E6%B3%95)
  - [1、快速生成 HTML 结构语法](#1%E5%BF%AB%E9%80%9F%E7%94%9F%E6%88%90-html-%E7%BB%93%E6%9E%84%E8%AF%AD%E6%B3%95)
  - [2、快速生成CSS样式语法](#2%E5%BF%AB%E9%80%9F%E7%94%9F%E6%88%90css%E6%A0%B7%E5%BC%8F%E8%AF%AD%E6%B3%95)
  - [3、快速格式化代码](#3%E5%BF%AB%E9%80%9F%E6%A0%BC%E5%BC%8F%E5%8C%96%E4%BB%A3%E7%A0%81)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->



> 原创思维导图，开源地址：https://github.com/JERRY-Z-J-R/JERRY-Mind

![](https://img-blog.csdnimg.cn/20210219020558153.png)


# Emmet 语法

`Emmet` 语法的前身是 `Zen coding`，它使用缩写，来提高 `html / css` 的编写速度,，`Vscode` 内部已经集成该语法

- 快速生成 HTML 结构语法
- 快速生成 CSS 样式语法

## 1、快速生成 HTML 结构语法

- 生成标签 直接输入标签名 按 `tab` 键即可 比如 `div` 然后 `tab` 键， 就可以生成 `<div></div>`
- 如果想要生成多个相同标签 加上 `*` 就可以了 比如 `div*3` 就可以快速生成3个 `div`
- 如果有父子级关系的标签，可以用 `>` 比如 `ul>li` 就可以了
- 如果有兄弟关系的标签，用 `+` 就可以了 比如 `div+p`
- 如果生成带有类名或者 `id` 名字的， 直接写 `.demo` 或者 `#two tab` 键就可以了
- 如果生成的 `div` 类名是有顺序的， 可以用 自增符号 `$`
- 如果想要在生成的标签内部写内容可以用 `{ }` 表示

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Emmet语法之快速生成HTML结构语法</title>
</head>

<body>
    <!-- div+Tab -->
    <div></div>
    <!-- table+Tab -->
    <table></table>
    <!-- div*6+Tab -->
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <!-- p*4+Tab -->
    <p></p>
    <p></p>
    <p></p>
    <p></p>
    <!-- ul>li+Tab -->
    <ul>
        <li></li>
    </ul>
    <!-- div>span+Tab -->
    <div><span></span></div>
    <!-- div+p+Tab -->
    <div></div>
    <p></p>
    <!-- .nav+Tab -->
    <div class="nav"></div>
    <!-- #banner+Tab -->
    <div id="banner"></div>
    <!-- p.one+Tab -->
    <p class="one"></p>
    <!-- span.gray+Tab -->
    <span class="gray"></span>
    <!-- ul>li#two+Tab -->
    <ul>
        <li id="two"></li>
    </ul>
    <!-- .demo*5+Tab -->
    <div class="demo"></div>
    <div class="demo"></div>
    <div class="demo"></div>
    <div class="demo"></div>
    <div class="demo"></div>
    <!-- .demo$*5+Tab -->
    <div class="demo1"></div>
    <div class="demo2"></div>
    <div class="demo3"></div>
    <div class="demo4"></div>
    <div class="demo5"></div>
    <!-- div{pink老师不是gay}+Tab -->
    <div>pink老师不是gay</div>
    <!-- div{他不喜欢男人}*6+Tab -->
    <div>他不喜欢男人</div>
    <div>他不喜欢男人</div>
    <div>他不喜欢男人</div>
    <div>他不喜欢男人</div>
    <div>他不喜欢男人</div>
    <div>他不喜欢男人</div>
    <!-- div{$}*6+Tab -->
    <div>1</div>
    <div>2</div>
    <div>3</div>
    <div>4</div>
    <div>5</div>
    <div>6</div>
</body>

</html>
```

## 2、快速生成CSS样式语法

CSS 基本采取简写形式即可

- 比如 `w200` 按 `tab` 可以 生成 `width: 200px;`
- 比如 `lh26px` 按 `tab` 可以生成 `line-height: 26px;`

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Emmet语法之快速生成CSS样式语法</title>
    <style>
        .one {
            /* tac+Tab */
            text-align: center;
            /* ti2e+Tab */
            text-indent: 2em;
            /* w+Tab */
            /* width: ; */
            /* h+Tab */
            /* height: ; */
            /* w24+Tab */
            width: 24px;
            /* h24+Tab */
            height: 24px;
            /* tdn+Tab */
            text-decoration: none;
        }
    </style>
</head>

<body>

</body>

</html>
```

## 3、快速格式化代码

`VSCode` 快速格式化代码：`shift+alt+f`
也可以设置当我们保存页面的时候自动格式化代码:

- 文件 ——>【首选项】——>【设置】
- 搜索 `emmet.include`
- 在 `settings.json` 下的【工作区设置】中添加以下语句：
  `"editor.formatOnType": true`
  `"editor.formatOnSave": true`
  
> 原创思维导图，开源地址：https://github.com/JERRY-Z-J-R/JERRY-Mind

![](https://img-blog.csdnimg.cn/20210131152353851.png)


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