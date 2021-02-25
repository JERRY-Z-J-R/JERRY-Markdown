---
title: 利用带命令提示符的安全模式剖解Windows密码 入门详解 - 精简归纳
date: 2020-10-13 19:56:01
categories:
- [个人教程]
- [Windows]
tags:
- Windows
- 安全模式
- 密码破解
---
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201013234117333.png)
<!--more-->
# 利用带命令提示符的安全模式剖解Windows密码 入门详解 - 精简归纳

> 原创内容，转载请注明出处！

---

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [利用带命令提示符的安全模式剖解Windows密码 入门详解 - 精简归纳](#%E5%88%A9%E7%94%A8%E5%B8%A6%E5%91%BD%E4%BB%A4%E6%8F%90%E7%A4%BA%E7%AC%A6%E7%9A%84%E5%AE%89%E5%85%A8%E6%A8%A1%E5%BC%8F%E5%89%96%E8%A7%A3windows%E5%AF%86%E7%A0%81-%E5%85%A5%E9%97%A8%E8%AF%A6%E8%A7%A3---%E7%B2%BE%E7%AE%80%E5%BD%92%E7%BA%B3)
- [一、说明](#%E4%B8%80%E8%AF%B4%E6%98%8E)
- [二、带命令提示符清除法](#%E4%BA%8C%E5%B8%A6%E5%91%BD%E4%BB%A4%E6%8F%90%E7%A4%BA%E7%AC%A6%E6%B8%85%E9%99%A4%E6%B3%95)
  - [(1)、重启Win7系统电脑按住F8键](#1%E9%87%8D%E5%90%AFwin7%E7%B3%BB%E7%BB%9F%E7%94%B5%E8%84%91%E6%8C%89%E4%BD%8Ff8%E9%94%AE)
  - [(2)、然后出现高级启动选项](#2%E7%84%B6%E5%90%8E%E5%87%BA%E7%8E%B0%E9%AB%98%E7%BA%A7%E5%90%AF%E5%8A%A8%E9%80%89%E9%A1%B9)
  - [(3)、选择【带命令提示符的安全模式】](#3%E9%80%89%E6%8B%A9%E5%B8%A6%E5%91%BD%E4%BB%A4%E6%8F%90%E7%A4%BA%E7%AC%A6%E7%9A%84%E5%AE%89%E5%85%A8%E6%A8%A1%E5%BC%8F)
  - [(4)、在出现的账号选择窗口中点击【Administrator】](#4%E5%9C%A8%E5%87%BA%E7%8E%B0%E7%9A%84%E8%B4%A6%E5%8F%B7%E9%80%89%E6%8B%A9%E7%AA%97%E5%8F%A3%E4%B8%AD%E7%82%B9%E5%87%BBadministrator)
  - [(5)、在命令提示符窗口中输入【net user Smile / add】](#5%E5%9C%A8%E5%91%BD%E4%BB%A4%E6%8F%90%E7%A4%BA%E7%AC%A6%E7%AA%97%E5%8F%A3%E4%B8%AD%E8%BE%93%E5%85%A5net-user-smile--add)
  - [(6)、接着继续输入【net localgroup administrators Smile /add】](#6%E6%8E%A5%E7%9D%80%E7%BB%A7%E7%BB%AD%E8%BE%93%E5%85%A5net-localgroup-administrators-smile-add)
  - [(7)、命令成功后继续输入【shutdown /r /t 5 /f】](#7%E5%91%BD%E4%BB%A4%E6%88%90%E5%8A%9F%E5%90%8E%E7%BB%A7%E7%BB%AD%E8%BE%93%E5%85%A5shutdown-r-t-5-f)
  - [(8)、最后电脑重启，选择刚刚设置Smile账号，进入即可](#8%E6%9C%80%E5%90%8E%E7%94%B5%E8%84%91%E9%87%8D%E5%90%AF%E9%80%89%E6%8B%A9%E5%88%9A%E5%88%9A%E8%AE%BE%E7%BD%AEsmile%E8%B4%A6%E5%8F%B7%E8%BF%9B%E5%85%A5%E5%8D%B3%E5%8F%AF)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

---


# 一、说明

开机密码大家都不陌生，我们手机上就可以有各种方式得开机密码。不过电脑上就只有一种数字的开机密码了。现在密码太多，有些朋友就混淆了。那么我们该如何破解呢？下面以win7系统为例，教大家破解开机密码的方法。

现在的中国用户基本都在使用win7系统，在使用过程中也会碰到一些人为问题。比如win7系统的开机密码忘记了。或者被别人恶意设置了电脑密码带不开该怎么办？这让很多小白束手无策。对此给大家带来了破解win7开机密码的图文教绍，希望能帮助到各位。

---

# 二、带命令提示符清除法

## (1)、重启Win7系统电脑按住F8键


## (2)、然后出现高级启动选项

## (3)、选择【带命令提示符的安全模式】
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201013234117333.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


## (4)、在出现的账号选择窗口中点击【Administrator】
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020101323412747.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)



## (5)、在命令提示符窗口中输入【net user Smile / add】
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201013234236541.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


## (6)、接着继续输入【net localgroup administrators Smile /add】



## (7)、命令成功后继续输入【shutdown /r /t 5 /f】

![在这里插入图片描述](https://img-blog.csdnimg.cn/2020101323413747.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

## (8)、最后电脑重启，选择刚刚设置Smile账号，进入即可
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201013234319594.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


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