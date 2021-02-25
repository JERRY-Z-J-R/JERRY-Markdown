---
title: 利用Gitee转接GitHub下载加速 简简单单 - 快快乐乐学会Git玩转GitHub(第二篇) 入门详解 - 精简归纳
date: 2020-10-24 06:00:00
categories: 
- [个人教程]
- [Git]
tags:
- Git
- GitHub
---

![封面](https://img-blog.csdnimg.cn/20201130224730571.jpg)

<!--more-->
# 利用Gitee转接GitHub下载加速 简简单单 - 快快乐乐

> 原创内容，转载请注明出处！


---

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [利用Gitee转接GitHub下载加速 简简单单 - 快快乐乐](#%E5%88%A9%E7%94%A8gitee%E8%BD%AC%E6%8E%A5github%E4%B8%8B%E8%BD%BD%E5%8A%A0%E9%80%9F-%E7%AE%80%E7%AE%80%E5%8D%95%E5%8D%95---%E5%BF%AB%E5%BF%AB%E4%B9%90%E4%B9%90)
- [一、说明](#%E4%B8%80%E8%AF%B4%E6%98%8E)
- [二、利用Gitee转接GitHub仓库](#%E4%BA%8C%E5%88%A9%E7%94%A8gitee%E8%BD%AC%E6%8E%A5github%E4%BB%93%E5%BA%93)
- [三、本地间接克隆GitHub仓库](#%E4%B8%89%E6%9C%AC%E5%9C%B0%E9%97%B4%E6%8E%A5%E5%85%8B%E9%9A%86github%E4%BB%93%E5%BA%93)
- [四、设置.git文件内的config文件](#%E5%9B%9B%E8%AE%BE%E7%BD%AEgit%E6%96%87%E4%BB%B6%E5%86%85%E7%9A%84config%E6%96%87%E4%BB%B6)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


---



# 一、说明

GitHub作为世界上最火的远程代码管理仓库以及最活跃最牛B的开源社区，可以说GitHub已经是全球程序员最爱的平台了，并且没有之一，没有之一！

但是作为国内的程序员来说，由于GitHub在中国没有成立专门的子公司，GitHub的服务器都在国外，所以国内范围内访问GitHub的速度非常慢，甚至某些时候就根本访问不了，而这还不是最严重的问题，关键问题在于当我们在GitHub中克隆某个远程仓库到本地计算机时，往往下载速度维持在（10~30 kb\s）的速度，这样的速度当我们需要克隆一个大型的项目时，是非常耗时的，而在提交大型代码时也是非常的漫长，所以诞生了许多的方法来改进GitHub的速度问题，而目前我认为最具简单性与速度性的方法就是利用国内目前最好的远程仓库平台Gitee来转接GitHub进而实现下载加速……

---

# 二、利用Gitee转接GitHub仓库

原理：我们借助Gitee的高速下载将GitHub上的仓库保存到Gitee中

![在这里插入图片描述](https://img-blog.csdnimg.cn/2020102612151324.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026121522465.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020102612154022.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026121551840.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026121600865.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026121610741.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


---

# 三、本地间接克隆GitHub仓库

原理：我们在本地直接克隆Gitee内的仓库，从而间接克隆GitHub内的仓库，由于Gitee是国内公司，服务器全部署在国内，所以克隆速度非常快

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026121624849.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026121634632.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026121642526.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026121650477.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


---

# 四、设置.git文件内的config文件

原理：当我们再克隆Gitee仓库到本地后，要将代码提交到远程仓库中时，git push后实际上是提交到了Gitee中的仓库，而GitHub中的仓库是没有变化的，要解决这个问题，我们就要设置本地的.git文件内的config文件，将远程仓库的地址从Gitee地址修改为GitHub的地址，这样当我们再git push时，文件就可以直接提交到GitHub中了，当然此时Gitee中的仓库就不会被更新了，这一点要注意

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026121706378.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026121717501.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026121728664.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026121735792.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026121743666.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020102612175267.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020102612180085.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026121808852.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026121816490.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

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