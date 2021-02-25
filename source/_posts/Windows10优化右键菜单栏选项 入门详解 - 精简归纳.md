---
title: Windows10优化右键菜单栏选项 入门详解 - 精简归纳
date: 2020-10-29 19:56:01
categories:
- [个人教程]
- [Windows]
tags:
- Windows
- 菜单栏
- 优化
---
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029102816319.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
<!--more-->

# Windows10优化右键菜单栏选项 入门详解 - 精简归纳

> 原创内容，转载请注明出处！

---

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Windows10优化右键菜单栏选项 入门详解 - 精简归纳](#windows10%E4%BC%98%E5%8C%96%E5%8F%B3%E9%94%AE%E8%8F%9C%E5%8D%95%E6%A0%8F%E9%80%89%E9%A1%B9-%E5%85%A5%E9%97%A8%E8%AF%A6%E8%A7%A3---%E7%B2%BE%E7%AE%80%E5%BD%92%E7%BA%B3)
- [一、说明](#%E4%B8%80%E8%AF%B4%E6%98%8E)
- [二、打开注册表](#%E4%BA%8C%E6%89%93%E5%BC%80%E6%B3%A8%E5%86%8C%E8%A1%A8)
- [三、进入HKEY_CLASSES_ROOT\Directory\Background\shell](#%E4%B8%89%E8%BF%9B%E5%85%A5hkey_classes_root%5Cdirectory%5Cbackground%5Cshell)
- [四、修改shell](#%E5%9B%9B%E4%BF%AE%E6%94%B9shell)
- [五、新建项](#%E4%BA%94%E6%96%B0%E5%BB%BA%E9%A1%B9)
  - [(1)、Open CMD Here](#1open-cmd-here)
  - [(2)、Open VSCode Here](#2open-vscode-here)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


---

# 一、说明

许多软件在安装之后会自动修改Windows10注册表的内容，从而在右键菜单栏中添加一些该软件的快捷功能，但实际上大部分情况却是：我们需要的软件快捷功能没有，我们不需要的软件快捷功能却有一大堆……，看着密密麻麻却没有任何用的Windows10右键菜单栏选项，该怎么办呢？凉拌是不可能的，当然要去Windows10注册表修改相关内容啊！（注：下面以添加CMD和VSCode的快捷入口举例）

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029102816319.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


---

# 二、打开注册表
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029102921881.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

---

# 三、进入HKEY_CLASSES_ROOT\Directory\Background\shell
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029103057655.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

---

# 四、修改shell

当我们需要清除右键菜单栏的相关快捷功能时就直接删除shell中的相关项即可……
当我们需要添加右键菜单栏的相关快捷功能时就在shell下新建项，并在该项的下面在新建command项……再在项内新建相关类型的量并编辑相关值……

---

# 五、新建项
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029103117961.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

## (1)、Open CMD Here
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029103146464.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029103319270.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029103334936.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029103348725.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

## (2)、Open VSCode Here
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029103423946.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029103442861.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029103506638.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029103520136.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)



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
