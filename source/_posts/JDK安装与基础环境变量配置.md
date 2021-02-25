---
title: JDK安装与基础环境变量配置
date: 2020-09-17 09:36:00
categories: 
- [个人教程]
- [Java]
tags:
- Java
- JDK
---

![在这里插入图片描述](https://img-blog.csdnimg.cn/2020091713323179.png)

<!--more-->
# JDK安装与基础环境变量配置

---

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [JDK安装与基础环境变量配置](#jdk%E5%AE%89%E8%A3%85%E4%B8%8E%E5%9F%BA%E7%A1%80%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F%E9%85%8D%E7%BD%AE)
- [一、下载](#%E4%B8%80%E4%B8%8B%E8%BD%BD)
- [二、安装](#%E4%BA%8C%E5%AE%89%E8%A3%85)
  - [(1)、双击.exe文件](#1%E5%8F%8C%E5%87%BBexe%E6%96%87%E4%BB%B6)
  - [(2)、全选安装工具](#2%E5%85%A8%E9%80%89%E5%AE%89%E8%A3%85%E5%B7%A5%E5%85%B7)
  - [(3)、修改JDK默认路径](#3%E4%BF%AE%E6%94%B9jdk%E9%BB%98%E8%AE%A4%E8%B7%AF%E5%BE%84)
  - [(4)、其他默认下一步](#4%E5%85%B6%E4%BB%96%E9%BB%98%E8%AE%A4%E4%B8%8B%E4%B8%80%E6%AD%A5)
  - [(5)、修改JRE默认路径](#5%E4%BF%AE%E6%94%B9jre%E9%BB%98%E8%AE%A4%E8%B7%AF%E5%BE%84)
- [三、配置环境变量](#%E4%B8%89%E9%85%8D%E7%BD%AE%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F)
  - [(1)、前提引入](#1%E5%89%8D%E6%8F%90%E5%BC%95%E5%85%A5)
  - [(2)、说明](#2%E8%AF%B4%E6%98%8E)
  - [(3)、配置环境变量步骤](#3%E9%85%8D%E7%BD%AE%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F%E6%AD%A5%E9%AA%A4)
    - [<1>、找到jdk bin目录，并复制地址栏地址备用](#1%E6%89%BE%E5%88%B0jdk-bin%E7%9B%AE%E5%BD%95%E5%B9%B6%E5%A4%8D%E5%88%B6%E5%9C%B0%E5%9D%80%E6%A0%8F%E5%9C%B0%E5%9D%80%E5%A4%87%E7%94%A8)
    - [<2>、找到环境变量并在path中编辑添加bin路径](#2%E6%89%BE%E5%88%B0%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F%E5%B9%B6%E5%9C%A8path%E4%B8%AD%E7%BC%96%E8%BE%91%E6%B7%BB%E5%8A%A0bin%E8%B7%AF%E5%BE%84)
    - [<3>、说明：](#3%E8%AF%B4%E6%98%8E)
      - [1、JAVA_HOME：](#1java_home)
      - [2、path：](#2path)
      - [3、classpath：](#3classpath)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


---

# 一、下载

JDK下载网站

[www.oracle.com](http://www.oracle.com) 甲骨文官网

![在这里插入图片描述](https://img-blog.csdnimg.cn/2020091713323179.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


例如下载了：jdk-8u131-windows-x64.exe

解释：jdk：java开发工具包，8u：8.0版本，131：第131次修改，windows-64x：windows平台64位系统（注明：64位系统可以向下兼容32位版本JDK）

---

# 二、安装

## (1)、双击.exe文件
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200917133416547.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


下一步

## (2)、全选安装工具

默认便是全选了
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200917133436150.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


## (3)、修改JDK默认路径

默认路径：C:\Program files\Java\jdk1.8.0-131

修改为：D:\Java\jdk1.8.0-131（也可为C盘外的其他盘）

（说明：JDK安装路径不可以在C盘，不可以带空格与中文）

## (4)、其他默认下一步

## (5)、修改JRE默认路径

在安装时会跳出JRE安装选项框，此时要修改JRE路径与JDK路径相同

默认路径：C:\Program files\Java\jre1.8.0-131

修改为：D:\Java\jre1.8.0-131（与JDK安装路径相同）

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200917133508925.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200917133527986.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

---

# 三、配置环境变量

## (1)、前提引入

在D:\Java\jdk1.8.0-131中找到bin目录，在bin目录中找到java.exe（java解释器）和javac.exe（java编译器），直接双击打开会发现一个黑框框一闪而过！说明.exe文件已经执行了，但是运行结果没有停留，我们看不到！

解决方法：在MS cmd/终端中执行java.exe和javac.exe便可成功解决！

<1>、win+R打开运行窗口

<2>、输入cmd打开终端

<3>、D:进入D盘

<4>、cd Java\jdk1.8.0-131\bin

<5>、javac（此时成功打开javac.exe）

<6>、java（此时成功打开java.exe）

写第一个java程序：

<1>、说明：此时还没有配置jdk环境变量，所以我们要去D:\Java\jdk1.8.0-131\bin中新建一个.txt文件然后修改文件名及后缀为HelloWorld.java文件

<2>、用记事本打开HelloWorld.java文件，编写第一个代码

```java
class HelloWorld {

	public static void main(String[] args) {
        System.out.println("HelloWorld");
    }
	
}
//注意英文符号应该是半角符号
```

<3>、在D:\Java\jdk1.8.0-131\bin下编译.java源文件

javac HelloWorld.java

（生成HelloWorld.class文件）

<4>、D:\Java\jdk1.8.0-131\bin下运行.class字节码文件

java HelloWorld

（注意：java命令默认只能加载.class文件，所以不能是java HelloWorld.class）

## (2)、说明

在上述步骤中，编译运行成功的关键是.java文件放在bin目录中，但是这样的文件组织方式会导致bin目录内部混乱，所以我们希望将.java文件单独组织到自己的文件中，但此时javac.exe与java.exe又只在bin中才能识别，所以产生了矛盾，所以我们要配置环境变量，让javac.exe与java.exe在任何路径下都可以识别！

## (3)、配置环境变量步骤

### <1>、找到jdk bin目录，并复制地址栏地址备用

例如，D:\APP\JAVA\jdk1.8.0_131\bin

### <2>、找到环境变量并在path中编辑添加bin路径

注意：

对于环境变量分别存在用户变量与系统变量path

优先级为：系统变量path > 用户变量path

因为某些时候两者都有path，为了避免优先级混乱导致错误，所以将bin地址放在系统变量path中的第一行！(也是为了提高优先级！)

### <3>、说明：

#### 1、JAVA_HOME：

本文环境变量的配置并没有配置JAVA_HOME，原因是JAVA_HOME是在Java Web中才用到的，因为本文是JAVA基础课程，所以本处并不配置JAVA_HOME

#### 2、path：

通俗理解，path对于JAVA的意义便是让javac.exe与java.exe摆脱路径的限制！

#### 3、classpath：

通俗理解，class对于JAVA的意思便是让.class文件摆脱路径的限制，也就是说，当环境变量中配置好了classpath后即便.java文件与.class文件不在同一路径下也可以成功编译运行，但是就目前JAVA基础的学习而言，通常将.java文件编译后便会自动在该目录下创建.class文件了，所以本文处于JAVA基础的考虑并没有配置classpath的环境变量


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

