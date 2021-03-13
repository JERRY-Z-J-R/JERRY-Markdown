---
title: 学会Git玩转GitHub(第四篇) 入门详解 - 精简归纳
date: 2020-10-24 04:00:00
categories: 
- [个人教程]
- [Git]
tags:
- Git
- GitHub
---

![封面](https://img-blog.csdnimg.cn/20201130224703593.jpg)

<!--more-->
# 学会Git玩转GitHub(第四篇) 入门详解 - 精简归纳

> 原创内容，转载请注明出处！


---

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [学会Git玩转GitHub(第四篇) 入门详解 - 精简归纳](#%E5%AD%A6%E4%BC%9Agit%E7%8E%A9%E8%BD%ACgithub%E7%AC%AC%E5%9B%9B%E7%AF%87-%E5%85%A5%E9%97%A8%E8%AF%A6%E8%A7%A3---%E7%B2%BE%E7%AE%80%E5%BD%92%E7%BA%B3)
- [一、Git管理远程仓库](#%E4%B8%80git%E7%AE%A1%E7%90%86%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93)
  - [(1)、使用远程仓库的目的](#1%E4%BD%BF%E7%94%A8%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93%E7%9A%84%E7%9B%AE%E7%9A%84)
  - [(2)、Git克隆操作](#2git%E5%85%8B%E9%9A%86%E6%93%8D%E4%BD%9C)
    - [<1>、说明：我们应该先将远程仓库克隆到自己的计算机上作为本地仓库然后才能进行提交操作！](#1%E8%AF%B4%E6%98%8E%E6%88%91%E4%BB%AC%E5%BA%94%E8%AF%A5%E5%85%88%E5%B0%86%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93%E5%85%8B%E9%9A%86%E5%88%B0%E8%87%AA%E5%B7%B1%E7%9A%84%E8%AE%A1%E7%AE%97%E6%9C%BA%E4%B8%8A%E4%BD%9C%E4%B8%BA%E6%9C%AC%E5%9C%B0%E4%BB%93%E5%BA%93%E7%84%B6%E5%90%8E%E6%89%8D%E8%83%BD%E8%BF%9B%E8%A1%8C%E6%8F%90%E4%BA%A4%E6%93%8D%E4%BD%9C)
    - [<2>、目的：将远程仓库（GitHub对应的项目）复制到本地](#2%E7%9B%AE%E7%9A%84%E5%B0%86%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93github%E5%AF%B9%E5%BA%94%E7%9A%84%E9%A1%B9%E7%9B%AE%E5%A4%8D%E5%88%B6%E5%88%B0%E6%9C%AC%E5%9C%B0)
    - [<3>、克隆远程仓库到本地仓库：](#3%E5%85%8B%E9%9A%86%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93%E5%88%B0%E6%9C%AC%E5%9C%B0%E4%BB%93%E5%BA%93)
    - [<4>、在本地仓库提交代码](#4%E5%9C%A8%E6%9C%AC%E5%9C%B0%E4%BB%93%E5%BA%93%E6%8F%90%E4%BA%A4%E4%BB%A3%E7%A0%81)
    - [<5>、使用push命令将本地仓库中的代码提交到远程仓库中](#5%E4%BD%BF%E7%94%A8push%E5%91%BD%E4%BB%A4%E5%B0%86%E6%9C%AC%E5%9C%B0%E4%BB%93%E5%BA%93%E4%B8%AD%E7%9A%84%E4%BB%A3%E7%A0%81%E6%8F%90%E4%BA%A4%E5%88%B0%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93%E4%B8%AD)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

---

# 一、Git管理远程仓库
## (1)、使用远程仓库的目的
作用：备份，实现代码共享集中化管理

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025234551734.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025234602168.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

## (2)、Git克隆操作
### <1>、说明：我们应该先将远程仓库克隆到自己的计算机上作为本地仓库然后才能进行提交操作！

### <2>、目的：将远程仓库（GitHub对应的项目）复制到本地

### <3>、克隆远程仓库到本地仓库：

```
git clone 远程仓库地址
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026003408229.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026003356916.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026003417998.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020102600342853.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
### <4>、在本地仓库提交代码
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026003650464.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026003700584.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/202010260037109.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
### <5>、使用push命令将本地仓库中的代码提交到远程仓库中
```
git push
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026003822698.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026003831821.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026003838958.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026003847792.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026004032472.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026004042997.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201026004052429.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


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