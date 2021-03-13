---
title: JAVA JDK 环境变量配置 入门详解 - 精简归纳
date: 2020-09-13 09:36:00
categories: 
- [个人教程]
- [Java]
tags:
- Java
- JDK
- 环境变量
---
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200913230551142.png)

<!--more-->

# JAVA JDK 环境变量配置 入门详解 - 精简归纳

---

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [JAVA JDK 环境变量配置 入门详解 - 精简归纳](#java-jdk-%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F%E9%85%8D%E7%BD%AE-%E5%85%A5%E9%97%A8%E8%AF%A6%E8%A7%A3---%E7%B2%BE%E7%AE%80%E5%BD%92%E7%BA%B3)
- [一、为什么java jdk 要配置环境变量](#%E4%B8%80%E4%B8%BA%E4%BB%80%E4%B9%88java-jdk-%E8%A6%81%E9%85%8D%E7%BD%AE%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F)
- [二、如何配置](#%E4%BA%8C%E5%A6%82%E4%BD%95%E9%85%8D%E7%BD%AE)
  - [(1)、首先，找到 jdk 的安装目录](#1%E9%A6%96%E5%85%88%E6%89%BE%E5%88%B0-jdk-%E7%9A%84%E5%AE%89%E8%A3%85%E7%9B%AE%E5%BD%95)
  - [(2)、如上图所示，点击“高级系统设置”，进入如下界面：](#2%E5%A6%82%E4%B8%8A%E5%9B%BE%E6%89%80%E7%A4%BA%E7%82%B9%E5%87%BB%E9%AB%98%E7%BA%A7%E7%B3%BB%E7%BB%9F%E8%AE%BE%E7%BD%AE%E8%BF%9B%E5%85%A5%E5%A6%82%E4%B8%8B%E7%95%8C%E9%9D%A2)
  - [(3)、再点击“环境变量”，进入如下界面：](#3%E5%86%8D%E7%82%B9%E5%87%BB%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F%E8%BF%9B%E5%85%A5%E5%A6%82%E4%B8%8B%E7%95%8C%E9%9D%A2)
  - [(4)、选择“系统变量”区域的“新建”功能，点击后，进入如下界面：](#4%E9%80%89%E6%8B%A9%E7%B3%BB%E7%BB%9F%E5%8F%98%E9%87%8F%E5%8C%BA%E5%9F%9F%E7%9A%84%E6%96%B0%E5%BB%BA%E5%8A%9F%E8%83%BD%E7%82%B9%E5%87%BB%E5%90%8E%E8%BF%9B%E5%85%A5%E5%A6%82%E4%B8%8B%E7%95%8C%E9%9D%A2)
  - [(5)、设置系统变量名为JAVA_HOME](#5%E8%AE%BE%E7%BD%AE%E7%B3%BB%E7%BB%9F%E5%8F%98%E9%87%8F%E5%90%8D%E4%B8%BAjava_home)
  - [(6)、至此，环境变量就已经设置完啦！](#6%E8%87%B3%E6%AD%A4%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F%E5%B0%B1%E5%B7%B2%E7%BB%8F%E8%AE%BE%E7%BD%AE%E5%AE%8C%E5%95%A6)
  - [(7)、再输入命令javac，结果如下图所示：](#7%E5%86%8D%E8%BE%93%E5%85%A5%E5%91%BD%E4%BB%A4javac%E7%BB%93%E6%9E%9C%E5%A6%82%E4%B8%8B%E5%9B%BE%E6%89%80%E7%A4%BA)
  - [(8)、说明：](#8%E8%AF%B4%E6%98%8E)
- [三、附](#%E4%B8%89%E9%99%84)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

---

# 一、为什么java jdk 要配置环境变量
配置环境变量，可以使 jdk 全局生效！
因为我们没有配置 jdk 的环境变量，所以在没有在 jdk/bin 目录下是运行不了 java.exe (java 解释器) 和 javac.exe (java编译器) 的，当然我们也可以去 jdk/bin 目录下运行 java 程序啊，但我们在 bin 目录下通过启动 java.exe，然后再通过 javac.exe 要把一个 java 文件编译成 class 文件，这个 class 文件就生成在 jdk/bin 目录里了，这样的文件组织方式显然是不好的，所以我们需要把 jdk 配置到 path 里面，这样在任何目录下（全局）都能运行 java.exe 和 javac.exe 来编译 java 文件了，这样就不会让 jdk/bin 目录里有许多我们的 java 文件和 class 文件。

---
# 二、如何配置

## (1)、首先，找到 jdk 的安装目录
以博主为例，进入这一层 C:\Program Files\Java\jdk1.8.0_121目录，复制以备后用。然后，通过“控制面板”进入“系统”属性，实际上直接选择“此电脑”点击右键选择“属性”即可：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200913225941475.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)



## (2)、如上图所示，点击“高级系统设置”，进入如下界面：
![在这里插入图片描述](https://img-blog.csdnimg.cn/202009132300046.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)



## (3)、再点击“环境变量”，进入如下界面：
![在这里插入图片描述](https://img-blog.csdnimg.cn/202009132303013.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)




## (4)、选择“系统变量”区域的“新建”功能，点击后，进入如下界面：

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200913230102852.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


## (5)、设置系统变量名为JAVA_HOME
变量值为C:\Program Files\Java\jdk1.8.0_121，点击“确定”，然后打开“系统变量”区域的Path，将这条语句 ;%JAVA_HOME%\bin 追加到 Path 变量值的最后面，如下图所示：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200913230417174.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


## (6)、至此，环境变量就已经设置完啦！
但是空口无凭啊，我们再验证一下，用事实说话。因此，打开“命令行窗口”，输入命令java，结果如下图所示：

![在这里插入图片描述](https://img-blog.csdnimg.cn/2020091323051357.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)



## (7)、再输入命令javac，结果如下图所示：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200913230551142.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)



## (8)、说明：

 <1>、如上图所示的结果，已经可以证明我们的环境变量配置成功啦！不过说实话，我们在C盘验证不是很好，因为配置环境变量就是为了在其它位置（如D盘）也可以运行 jdk，我们都把 jdk 安装到C盘了，再在C盘进行验证就有些取巧了，因为就算环境变量没有配置成功，如果我们进入相应的安装目录下，也是可以运行 jdk 的。因此，我们来一个狠的，直接在D盘的根目录下创建一个.java文件，然后在“命令行窗口”编译并运行，如果这样做还能成功的话，那毫无疑问，环境变量我们肯定配置成功啦！

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200913230658735.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)



如上图所示，我们先在D盘的根目录下创建一个名为 HelloWorld.txt 文件，输入代码，然后我们再修改文件的后缀 .txt 为.java即可。最后，在“命令行窗口”输入命令

观察运行结果，显然我们的环境变量配置成功啦！

<2>、为啥要配置 JAVA_HOME，一定要用 JAVA_HOME 命名吗？

我们电脑如果装了多个版本的 jdk，我们只需要在 JAVA_HOME 中把 jdk 的目录添加进去，而不用在 path 里面加 bin 目录的路径
因为有些开发工具，如（eclipse，IDEA, tomcat）都会去扫描你的JAVA_HOME 变量，看看你的电脑装了几个版本的 jdk。可以不用 JAVA_HOME 这个名字当参数名，那么有些软件启动需要 JAVA_HOME，例如 tomcat，当你不用这个命名，你就需要去修改 tomcat 的 bin 目录下的 catalina.bat 文件,才能启动 tomcat，何必呢？

<3>、我们为什么没有配置 CLASSPATH 变量？

jdk1.5 之后就不用再配置 CLASSPATH了，当然，我们为了保证向下兼容，也可以配置上为好！

---

# 三、附
> 本文第二部分内容来源于：<https://blog.csdn.net/qq_35246620/article/details/61208961?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522159996354219195188335008%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=159996354219195188335008&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_click~default-2-61208961.pc_ecpm_v3_pc_rank_v3&utm_term=jdk%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F%E9%85%8D%E7%BD%AE&spm=1018.2118.3001.4187>
> 

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