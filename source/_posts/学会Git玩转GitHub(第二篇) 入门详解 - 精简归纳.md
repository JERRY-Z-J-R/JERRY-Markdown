---
title: 学会Git玩转GitHub(第二篇) 入门详解 - 精简归纳
date: 2020-10-24 01:00:00
categories: 
- [个人教程]
- [Git]
tags:
- Git
- GitHub
---

![封面](https://img-blog.csdnimg.cn/20201130224703593.jpg)

<!--more-->
# 学会Git玩转GitHub(第二篇) 入门详解 - 精简归纳

> 原创内容，转载请注明出处！

---

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [学会Git玩转GitHub(第二篇) 入门详解 - 精简归纳](#%E5%AD%A6%E4%BC%9Agit%E7%8E%A9%E8%BD%ACgithub%E7%AC%AC%E4%BA%8C%E7%AF%87-%E5%85%A5%E9%97%A8%E8%AF%A6%E8%A7%A3---%E7%B2%BE%E7%AE%80%E5%BD%92%E7%BA%B3)
- [一、目的](#%E4%B8%80%E7%9B%AE%E7%9A%84)
- [二、Git的下载及安装](#%E4%BA%8Cgit%E7%9A%84%E4%B8%8B%E8%BD%BD%E5%8F%8A%E5%AE%89%E8%A3%85)
- [三、初次使用Git前的配置](#%E4%B8%89%E5%88%9D%E6%AC%A1%E4%BD%BF%E7%94%A8git%E5%89%8D%E7%9A%84%E9%85%8D%E7%BD%AE)
- [四、Git理论基础](#%E5%9B%9Bgit%E7%90%86%E8%AE%BA%E5%9F%BA%E7%A1%80)
  - [(1)、Git记录的是什么](#1git%E8%AE%B0%E5%BD%95%E7%9A%84%E6%98%AF%E4%BB%80%E4%B9%88)
  - [(2)、Git的三棵树](#2git%E7%9A%84%E4%B8%89%E6%A3%B5%E6%A0%91)
- [五、查看工作状态和历史提交](#%E4%BA%94%E6%9F%A5%E7%9C%8B%E5%B7%A5%E4%BD%9C%E7%8A%B6%E6%80%81%E5%92%8C%E5%8E%86%E5%8F%B2%E6%8F%90%E4%BA%A4)
  - [(1)、查看状态](#1%E6%9F%A5%E7%9C%8B%E7%8A%B6%E6%80%81)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


---

# 一、目的

通过Git这个版本控制系统管理本地项目同时管理GitHub平台托管项目代码！

---

# 二、Git的下载及安装

官网下载地址：<www.git-scm.com/download/win>

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025185603832.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
双击.exe文件安装：

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025185700957.png#pic_center)

除了修改安装路径外，其他步骤一律无脑下一步……

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025185831327.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025185838631.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025185847186.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

安装完成后，右键会有Git的快速访问通道，点击即可快速在当前目录下打开Git，当然在cmd命令行中同样可以打开Git

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025190330753.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025190757309.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


---

# 三、初次使用Git前的配置

在命令行模式里输入以下命令：

```
git config --global user.name "用户名"		//配置Git用户名
git config --global user.email "邮箱"		 //配置Git用户邮箱
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025190414960.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

配置后输入：

```
git config --list	//列出配置列表
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025190441852.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

若成功列出了用户名与邮箱，那么便是配置成功了！

---

# 四、Git理论基础

## (1)、Git记录的是什么

Git会将每一个版本独立保存！

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025191138993.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025191148649.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

## (2)、Git的三棵树
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020102519121720.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025191327881.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

```
git init	
//初始化一个Git仓库
//（自动生成一个.git隐藏文件夹，不要改动此文件夹，否则会发生错误）
```
方式一、直接利用cmd命令行操作
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025192007108.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
方式二、直接在打开Git操作
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025192025644.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025192037216.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

所在目录为工作目录，也就是”第一课树“，该目录下存在.git文件夹，该文件夹就是管理跟踪版本信息的！

```
git add		//将文件提交到暂存区
```

在工作区创建一个README.md文件，这是项目的说明文档

将该说明文档添加到暂存区中，若没有任何提示则表明提交成功

![在这里插入图片描述](https://img-blog.csdnimg.cn/2020102519223793.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025192245738.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

```
git commit -m ""	//将文件提交到Git仓库，并添加提交说明
```

提交成功后，会出现一段提示，表明提交成功，并标明一些基本格式信息

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025192355353.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


同理：再在工作区中创建一个LICENSE文件，该文件内注明MIT版权协议

（MIT版权协议：所有开源协议中最为宽松的一种！外界引用自己的项目代码时只需要包含该文件就可以了，且自己的项目代码可以被用于大部分形式及用途）

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025192413829.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

---

# 五、查看工作状态和历史提交

## (1)、查看状态

```
git status	
//用于显示工作目录和暂存区的状态，使用此命令能看到那些修改被暂存到了,
//哪些没有, 哪些文件没有被Git tracked到。
//git status不显示已经commit到项目历史中去的信息。
//看项目历史的信息要使用git log
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025192819949.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

列出未跟踪文件，并给出建议可以通过add命令将其添加到暂存区

我们将其add入暂存区，再git status

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025192852912.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

之后我们再git commit -m "add a LICENSE file"

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025193046424.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


突然我们发现在LICENSE文件中忘记注明时间及作者了，所以我们直接在工作区中直接修改LICENSE文件

![在这里插入图片描述](https://img-blog.csdnimg.cn/2020102519311255.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025193119259.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
之后我们再git status

显示：

On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)（使用“ git add <文件> ...”更新将提交的内容）
  (use "git restore <file>..." to discard changes in working directory)（使用“ git restore <文件> ...”放弃工作目录中的更改，即：用原来的覆盖刚刚修改的）
        modified:   LICENSE

no changes added to commit (use "git add" and/or "git commit -a")


![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025193356262.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


接下来我们输入：

```
git restore LICENSE
```


然后我们再打开LICENSE文件，发现文件又退回修改之前的状态了，因为这是将原来以及提交的文件覆盖修改的文件，所以这个命令使用时一定要注意！

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025193502104.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


现在我们再把LICENSE文件重新修改

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025193523664.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


再输入git status回到上上步状态

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025193539513.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

此时我们使用git restore <file>...的上一个建议git add <file>...并在最后git status

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025193556432.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

来到这步时，我们先不将其commit到Git仓库，而是再对LICENSE文件进行修改

在修改之后我们再次git status

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025193856879.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


此时会发现出现了两个LICENSE文件，其中上一个文件是已经提交到暂存区中的文件，而下面一个文件则是在工作目录中最后被修改了的但还未跟踪的那一个文件

如果此时直接输入git commit -m""提交的就是第一个LICENSE文件，也就是原本在暂存区中的LICENSE文件

而假如需要提交工作区中的那一个LICENSE文件（也就是：最后修改过的那一个LICENSE文件）的话，需要先git add将该文件覆盖暂存区中的那一个LICENSE文件，之后再来git commit -m""，这样提交到Git仓库的才是最后修改的哪一个LICENSE文件

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201025194204462.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

```
git log		//查看历史提交记录，排序是从近到远
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/2020102519424477.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


可以发现，在列出的提交记录中，每一次记录上方都有一串值，这个是Git为每一个提交所标记的ID值，全世界唯一标记对应这一次提交！这在超大型项目管理中才不会发生混乱！


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
