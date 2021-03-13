---
title: Windows & Linux 安装使用 Vim 编辑器 入门说明 - 精简归纳
date: 2020-08-25 00:00:00
categories: 
- [个人教程]
- [Windows]
- [Linux]
tags:
- Windows
- Linux
- Vi
- Vim
---
![Linux Vim](https://img-blog.csdnimg.cn/20200825120022313.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
<!--more-->

# Windows & Linux 安装使用 Vim 编辑器 入门说明 - 精简归纳

> 原创内容，转载请注明出处！

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Windows & Linux 安装使用 Vim 编辑器 入门说明 - 精简归纳](#windows--linux-%E5%AE%89%E8%A3%85%E4%BD%BF%E7%94%A8-vim-%E7%BC%96%E8%BE%91%E5%99%A8-%E5%85%A5%E9%97%A8%E8%AF%B4%E6%98%8E---%E7%B2%BE%E7%AE%80%E5%BD%92%E7%BA%B3)
- [一、Vim 简单介绍](#%E4%B8%80vim-%E7%AE%80%E5%8D%95%E4%BB%8B%E7%BB%8D)
  - [(1)、Linux vi / Vim 介绍](#1linux-vi--vim-%E4%BB%8B%E7%BB%8D)
  - [(2)、什么是 Vim？](#2%E4%BB%80%E4%B9%88%E6%98%AF-vim)
- [二、Vim 的安装](#%E4%BA%8Cvim-%E7%9A%84%E5%AE%89%E8%A3%85)
  - [(1)、Windows](#1windows)
    - [<1>、进入网站下载 Windows 相应版本](#1%E8%BF%9B%E5%85%A5%E7%BD%91%E7%AB%99%E4%B8%8B%E8%BD%BD-windows-%E7%9B%B8%E5%BA%94%E7%89%88%E6%9C%AC)
    - [<2>、下载完成后点击 .exe 文件安装](#2%E4%B8%8B%E8%BD%BD%E5%AE%8C%E6%88%90%E5%90%8E%E7%82%B9%E5%87%BB-exe-%E6%96%87%E4%BB%B6%E5%AE%89%E8%A3%85)
    - [<3>、 配置环境变量](#3-%E9%85%8D%E7%BD%AE%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F)
  - [(2)、Linux](#2linux)
    - [<1>、打开终端](#1%E6%89%93%E5%BC%80%E7%BB%88%E7%AB%AF)
    - [<2>、输入命令下载安装 Vim](#2%E8%BE%93%E5%85%A5%E5%91%BD%E4%BB%A4%E4%B8%8B%E8%BD%BD%E5%AE%89%E8%A3%85-vim)
  - [(3)、如果上面的步骤成功完成，那么 Vim 便安装好了](#3%E5%A6%82%E6%9E%9C%E4%B8%8A%E9%9D%A2%E7%9A%84%E6%AD%A5%E9%AA%A4%E6%88%90%E5%8A%9F%E5%AE%8C%E6%88%90%E9%82%A3%E4%B9%88-vim-%E4%BE%BF%E5%AE%89%E8%A3%85%E5%A5%BD%E4%BA%86)
- [三、利用  Vim 编写代码](#%E4%B8%89%E5%88%A9%E7%94%A8--vim-%E7%BC%96%E5%86%99%E4%BB%A3%E7%A0%81)
  - [(1)、首先打开 Windows \ Linux 终端](#1%E9%A6%96%E5%85%88%E6%89%93%E5%BC%80-windows-%5C-linux-%E7%BB%88%E7%AB%AF)
  - [(2)、利用 cd 命令 切换到你将要保存代码的路径下](#2%E5%88%A9%E7%94%A8-cd-%E5%91%BD%E4%BB%A4-%E5%88%87%E6%8D%A2%E5%88%B0%E4%BD%A0%E5%B0%86%E8%A6%81%E4%BF%9D%E5%AD%98%E4%BB%A3%E7%A0%81%E7%9A%84%E8%B7%AF%E5%BE%84%E4%B8%8B)
  - [(3)、输入命令打开 Vim](#3%E8%BE%93%E5%85%A5%E5%91%BD%E4%BB%A4%E6%89%93%E5%BC%80-vim)
  - [(4)、Vim 中打开了 test.c 文件](#4vim-%E4%B8%AD%E6%89%93%E5%BC%80%E4%BA%86-testc-%E6%96%87%E4%BB%B6)
  - [(5)、打开 Vim 编辑模式](#5%E6%89%93%E5%BC%80-vim-%E7%BC%96%E8%BE%91%E6%A8%A1%E5%BC%8F)
  - [(6)、利用 Vim 编写代码](#6%E5%88%A9%E7%94%A8-vim-%E7%BC%96%E5%86%99%E4%BB%A3%E7%A0%81)
  - [(7)、保存并退出 Vim](#7%E4%BF%9D%E5%AD%98%E5%B9%B6%E9%80%80%E5%87%BA-vim)
  - [(8)、编译、运行代码](#8%E7%BC%96%E8%AF%91%E8%BF%90%E8%A1%8C%E4%BB%A3%E7%A0%81)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


# 一、Vim 简单介绍

## (1)、Linux vi / Vim 介绍

*所有的 Unix Like 系统都会内建 vi 文书编辑器，其他的文书编辑器则不一定会存在。*

*但是目前我们使用比较多的是 Vim 编辑器。*

*Vim 具有程序编辑的能力，可以主动的以字体颜色辨别语法的正确性，方便程序设计。*

## (2)、什么是 Vim？

*Vim 是从 vi 发展出来的一个文本编辑器。代码补完、编译及错误跳转等方便编程的功能特别丰富，在程序员中被广泛使用。*

*简单的来说 ，vi 是老式的字处理器，不过功能已经很齐全了，但是还是有可以进步的地方。Vim 则可以说是程序开发者的一项很好用的工具。*

*连 Vim 的官方网站 (<http://www.vim.org/>) 自己也说 Vim 是一个程序开发工具而不是文字处理软件。*

> 以上简介来源于：菜鸟教程 <https://www.runoob.com/>

---

# 二、Vim 的安装

## (1)、Windows

> *说明：本文以 Windows 10 为例*

### <1>、进入网站下载 Windows 相应版本

<https://vim.en.softonic.com/>

### <2>、下载完成后点击 .exe 文件安装

*建议：选择安装路径时不要选择默认路径，不要选择带有中文的路径，其他选项默认下一步即可*

### <3>、 配置环境变量
*打开：系统属性、高级、环境变量；*

*找到：系统变量；*

*点击：Path；*

*点击：编辑；*

*点击：新建；*

*将 Vim 刚才安装的绝对路径复制进去；*

*点击：确定*

## (2)、Linux

> *说明：本文以 Linux Ubuntu 20.04.1 为例*

### <1>、打开终端

*快捷键：Ctrl + Alt + T*

### <2>、输入命令下载安装 Vim

```
sudo apt-get install vim
```

*Linux 会自动检测并下载安装*

## (3)、如果上面的步骤成功完成，那么 Vim 便安装好了

*可以在命令行输入下面的命令，即可成功打开  Vim：*

```
vim
```

Windows：
![Windows Vim](https://img-blog.csdnimg.cn/20200825115949478.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


Linux：
![Linux Vim](https://img-blog.csdnimg.cn/20200825120022313.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

---

# 三、利用  Vim 编写代码

> *此处 Windows Linux 均相同，下面以 Linux 举例*

## (1)、首先打开 Windows \ Linux 终端

*Windown：Win + R 打开运行会话框，输入 cmd，点击确定按钮或键盘敲击回车键即可进入命令行。*

*Linux：快捷键：Ctrl + Alt + T，即可进入命令行。*

## (2)、利用 cd 命令 切换到你将要保存代码的路径下
![cd 切换路径](https://img-blog.csdnimg.cn/20200825120155162.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


## (3)、输入命令打开 Vim 

```
vim test.c
```

*此时，Vim便会在当前目录下新建一个 test.c 空白文件（当前目录下原先不存在 test.c 文件时），否则会自动打开原先便存在的 test.c 文件*
![vim test.c](https://img-blog.csdnimg.cn/20200825120243955.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


## (4)、Vim 中打开了 test.c 文件
*左下角显示：test.c*
![Vim 中打开了 test.c 文件](https://img-blog.csdnimg.cn/20200825120356996.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


## (5)、打开 Vim 编辑模式

*点击键盘 i 键，左下角显示：INSERT，表示进入编辑模式*
![编辑模式](https://img-blog.csdnimg.cn/20200825120428413.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


## (6)、利用 Vim 编写代码
![编写代码](https://img-blog.csdnimg.cn/20200825120950789.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)



## (7)、保存并退出 Vim

*写完后，按下 Esc 键退出编辑模式，随后按下 Shift + 冒号，此时左下角显示一个冒号（在 Vim 中任何功能的操作都是以命令来识别，而 “冒号” 即表示等待输入命令），再在冒号后输入：wq 表示保存代码并退出 Vim （只输入 q 表示不保存只退出）*
![冒号](https://img-blog.csdnimg.cn/20200825120539407.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![wq](https://img-blog.csdnimg.cn/20200825120603899.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)



## (8)、编译、运行代码
![编译、运行代码](https://img-blog.csdnimg.cn/20200825120627281.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

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
