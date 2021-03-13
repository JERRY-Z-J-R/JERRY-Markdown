---
title: Java JDK 安装目录及其子目录含义 入门详解 - 精简归纳
date: 2020-08-30 09:36:00
categories: 
- [个人教程]
- [Java]
tags:
- Java
- JDK
---

![JDK 安装目录及其子目录结构图](https://img-blog.csdnimg.cn/20200830124817620.png)

<!--more-->
# Java JDK 安装目录及其子目录含义 入门详解 - 精简归纳
---

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Java JDK 安装目录及其子目录含义 入门详解 - 精简归纳](#java-jdk-%E5%AE%89%E8%A3%85%E7%9B%AE%E5%BD%95%E5%8F%8A%E5%85%B6%E5%AD%90%E7%9B%AE%E5%BD%95%E5%90%AB%E4%B9%89-%E5%85%A5%E9%97%A8%E8%AF%A6%E8%A7%A3---%E7%B2%BE%E7%AE%80%E5%BD%92%E7%BA%B3)
- [一、JDK 安装目录及其子目录结构图](#%E4%B8%80jdk-%E5%AE%89%E8%A3%85%E7%9B%AE%E5%BD%95%E5%8F%8A%E5%85%B6%E5%AD%90%E7%9B%AE%E5%BD%95%E7%BB%93%E6%9E%84%E5%9B%BE)
- [二、认识 JDK 与 JRE](#%E4%BA%8C%E8%AE%A4%E8%AF%86-jdk-%E4%B8%8E-jre)
  - [(1)、啥是 JDK ?](#1%E5%95%A5%E6%98%AF-jdk-)
  - [(2)、啥是 JRE ?](#2%E5%95%A5%E6%98%AF-jre-)
  - [(3)、JDK 与 JRE 的关系](#3jdk-%E4%B8%8E-jre-%E7%9A%84%E5%85%B3%E7%B3%BB)
    - [<1>、区别](#1%E5%8C%BA%E5%88%AB)
    - [<2>、联系](#2%E8%81%94%E7%B3%BB)
    - [<3>、包含](#3%E5%8C%85%E5%90%AB)
- [三、JDK 各个文件夹含义详解](#%E4%B8%89jdk-%E5%90%84%E4%B8%AA%E6%96%87%E4%BB%B6%E5%A4%B9%E5%90%AB%E4%B9%89%E8%AF%A6%E8%A7%A3)
  - [(1)、D:\Program\Java\jdk 目录](#1d%5Cprogram%5Cjava%5Cjdk-%E7%9B%AE%E5%BD%95)
    - [<1>、D:\Program\Java\jdk](#1d%5Cprogram%5Cjava%5Cjdk)
    - [<2>、--jdk\bin](#2--jdk%5Cbin)
    - [<3>、--jdk\lib](#3--jdk%5Clib)
    - [<4>、--jdk\jre](#4--jdk%5Cjre)
    - [<5>、--jdk\include](#5--jdk%5Cinclude)
  - [(2)、D:\Program\Java\jdk\jre 目录](#2d%5Cprogram%5Cjava%5Cjdk%5Cjre-%E7%9B%AE%E5%BD%95)
    - [<1>、D:\Program\Java\jdk\jre](#1d%5Cprogram%5Cjava%5Cjdk%5Cjre)
    - [<2>、 --jdk\jre\bin](#2---jdk%5Cjre%5Cbin)
    - [<3>、--jdk\jre\lib](#3--jdk%5Cjre%5Clib)
      - [1、rt.jar](#1rtjar)
      - [2、charsets.jar](#2charsetsjar)
      - [3、--jdk\jre\lib\ext](#3--jdk%5Cjre%5Clib%5Cext)
      - [4、--jdk\jre\lib\security](#4--jdk%5Cjre%5Clib%5Csecurity)
      - [5、--jdk\jre\lib\applet](#5--jdk%5Cjre%5Clib%5Capplet)
      - [6、--jdk\jre\lib\fonts](#6--jdk%5Cjre%5Clib%5Cfonts)
  - [(3)、为什么 Java 目录中会存在两个 jre 目录以及三个 lib 目录，他们的作用和区别又是什么？](#3%E4%B8%BA%E4%BB%80%E4%B9%88-java-%E7%9B%AE%E5%BD%95%E4%B8%AD%E4%BC%9A%E5%AD%98%E5%9C%A8%E4%B8%A4%E4%B8%AA-jre-%E7%9B%AE%E5%BD%95%E4%BB%A5%E5%8F%8A%E4%B8%89%E4%B8%AA-lib-%E7%9B%AE%E5%BD%95%E4%BB%96%E4%BB%AC%E7%9A%84%E4%BD%9C%E7%94%A8%E5%92%8C%E5%8C%BA%E5%88%AB%E5%8F%88%E6%98%AF%E4%BB%80%E4%B9%88)
    - [<1>、两个 jre 目录](#1%E4%B8%A4%E4%B8%AA-jre-%E7%9B%AE%E5%BD%95)
      - [1、D:\Program\Java\jre](#1d%5Cprogram%5Cjava%5Cjre)
      - [2、D:\Program\Java\jdk\jre](#2d%5Cprogram%5Cjava%5Cjdk%5Cjre)
      - [3、区别及联系](#3%E5%8C%BA%E5%88%AB%E5%8F%8A%E8%81%94%E7%B3%BB)
    - [<2>、三个 lib 目录](#2%E4%B8%89%E4%B8%AA-lib-%E7%9B%AE%E5%BD%95)
      - [1、jre 下的 lib](#1jre-%E4%B8%8B%E7%9A%84-lib)
      - [2、jdk 下的 lib](#2jdk-%E4%B8%8B%E7%9A%84-lib)
      - [3、jdk 下的 jre 下的 lib](#3jdk-%E4%B8%8B%E7%9A%84-jre-%E4%B8%8B%E7%9A%84-lib)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

---
# 一、JDK 安装目录及其子目录结构图
> 这里以 JDK 1.8.0_231 版本为例
> JDK 安装在了：D:\Program\Java 目录下


当 JDK 安装完成后，在安装目录下除了 jdk 文件夹， 还会出现一个 jre 文件夹，而 jdk 文件夹内部也包含一个 jre 文件夹……，具体含义待会再说，先看一下 JDK 安装目录及其子目录结构图： 

![JDK 安装目录及其子目录结构图](https://img-blog.csdnimg.cn/20200830124817620.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

---

# 二、认识 JDK 与 JRE
## (1)、啥是 JDK ?
JDK 即 Java SDK （全称：Java 程序开发的工具包），JDK 是整个 Java 的核心，包括了 Java 的开发环境和运行环境，以及一堆 Java 工具 (tools.jar) 和 Java 基础的类库 (rt.jar) 等。
## (2)、啥是 JRE ?
JRE 即 Java 运行环境，是运行 JAVA 程序所必须的环境的集合，包含 JVM （JAVA 虚拟机）标准实现、Java 核心类库 (API) 及支持文件，但不包含开发工具（编译器、调试器等）。


## (3)、JDK 与 JRE 的关系 

### <1>、区别
JDK 是开发工具包，是用来开发 Java 程序的，也就自然是面对 Java 的程序开发人员，而 JRE 是只是运行环境，面向的是 Java 程序的使用者。也就是说，如果要使用 Java 开发程序，则必须安装 JDK，但如果只是想运行 Java 程序，那只需要安装JRE 即可。

### <2>、联系
> 参考以下Java源文件的编译和执行过程

1、Java 源文件 (.java) 经过 Java 编译器 (javac.exe) 编译以后形成 JVM 可运行的字节码 (.class) 文件。

2、运行 Java 解释器 (java.exe) 即可将 JVM 上运行的目标代码（字节码，即 .class 文件）解释成为具体平台的机器码（通常为：二进制码），也就可以运行该 Java 程序了。

3、任何一台机器只要配备了 Java 解释器，就可以运行这个程序，而不管这种字节码是在何种平台上生成的。但要注意的是 Java 解释器只是一个基于 JVM 平台的程序，所以它不能单独执行，必须依赖于JVM。

### <3>、包含
![包含关系](https://img-blog.csdnimg.cn/20200830132432440.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
由上图可知：JDK 包含 JRE 包含 JVM
所以，安装 JDK 就间接安装 JRE 及 JVM 了

---

# 三、JDK 各个文件夹含义详解
## (1)、D:\Program\Java\jdk 目录

### <1>、D:\Program\Java\jdk
jdk 根目录，包含版权、许可及 README 文件以及Java核心平台API的源文件归档 (src.zip)。

### <2>、--jdk\bin
jdk开发工具可执行文件目录，里面包含有 javac.exe、java.exe 等可执行程序。

### <3>、--jdk\lib
jdk 开发工具使用的类库目录，主要包括 tools.jar 和 dt.jar。

### <4>、--jdk\jre
jdk 开发工具所使用的 Java 运行时环境的根目录，除了文档外，它与可部署的 jre 完全相同。

### <5>、--jdk\include
c 的头文件，用与支持 native-code 库使用 jvm Debugger（虚拟机调试器）接口。


## (2)、D:\Program\Java\jdk\jre 目录

### <1>、D:\Program\Java\jdk\jre
Java 运行环境存放目录。

### <2>、 --jdk\jre\bin
jre 执行文件及 DLL 库，可执行文件与 jdk\bin 相同，不必将该目录放在 PATH 环境变量中。

### <3>、--jdk\jre\lib
 Java 程序运行时环境使用的代码库、属性设置和资源文件，主要包括：

#### 1、rt.jar
系统引导库（构成Java平台核心API的RunTime 类）。

#### 2、charsets.jar
字符转换类及其它与国际化和本地化有关的类。

#### 3、--jdk\jre\lib\ext
Java 平台扩展类库的缺省安装目录。例如 JavaHelp jar 就可以放在此目录下。

#### 4、--jdk\jre\lib\security
包含用于安全管理的文件。这些文件包括安全策略 (java.policy) 和安全属性 (java.security) 文件。

#### 5、--jdk\jre\lib\applet
对 applet 支持的一些资源文件。

#### 6、--jdk\jre\lib\fonts
TrueType 字体文件。

 

## (3)、为什么 Java 目录中会存在两个 jre 目录以及三个 lib 目录，他们的作用和区别又是什么？


### <1>、两个 jre 目录
#### 1、D:\Program\Java\jre
可部署的 JRE。

#### 2、D:\Program\Java\jdk\jre
jdk 中自带并使用的 JRE。
#### 3、区别及联系
总体来说，两个 JRE 文件夹的内容基本相同，区别主要体现在工作的职责上，也就是不同的 JRE 负责不同的工作范围。

如果只是要执行 Java 程序，则只需要 Java 目录下的 JRE 即可。如果要开发 Java 程序，则需要 JDK 中的 JRE。比如我们使用 javac.exe 来编译 Java 程序时，系统会优先使用 jdk\bin 下的可执行文件，使用的运行环境也是 jdk 下的 jre。

![两个JRE](https://img-blog.csdnimg.cn/20200830144555319.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

### <2>、三个 lib 目录

D:\Program\Java\jre\lib：jre下的。
D:\Program\Java\jdk\lib：jdk下的。
D:\Program\Java\jdk\jre\lib：jdk\jre下的。

#### 1、jre 下的 lib
只是运行 java 程序的 jar 包，是为 JVM 运行时候用的，包括所有的标准类库和扩展类等。

#### 2、jdk 下的 lib
包括 java 开发环境的 jar 包，是给 JDK 用的，例如 JDK 下有一些工具，可能要用该目录中的文件，比如编译器等。

#### 3、jdk 下的 jre 下的 lib
是开发环境中，运行时需要的 jar 包。最典型的就是导入的外部驱动 jar 包，因为编译时，系统找的是 jdk 下的 jre，而不是最外层的 jre。


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
