---
title: 学会Git玩转GitHub(第一篇) 入门详解 - 精简归纳
date: 2020-10-24 00:00:02
categories: 
- [个人教程]
- [Git]
tags:
- Git
- GitHub
---

![封面](https://img-blog.csdnimg.cn/20201130224730573.jpg)

<!--more-->

# 学会Git玩转GitHub(第一篇) 入门详解 - 精简归纳

> 原创内容，转载请注明出处！

---

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [学会Git玩转GitHub(第一篇) 入门详解 - 精简归纳](#%E5%AD%A6%E4%BC%9Agit%E7%8E%A9%E8%BD%ACgithub%E7%AC%AC%E4%B8%80%E7%AF%87-%E5%85%A5%E9%97%A8%E8%AF%A6%E8%A7%A3---%E7%B2%BE%E7%AE%80%E5%BD%92%E7%BA%B3)
- [一、使用GitHub](#%E4%B8%80%E4%BD%BF%E7%94%A8github)
  - [(1)、目的](#1%E7%9B%AE%E7%9A%84)
  - [(2)、基本概念](#2%E5%9F%BA%E6%9C%AC%E6%A6%82%E5%BF%B5)
    - [<1>、仓库（Repository）](#1%E4%BB%93%E5%BA%93repository)
    - [<2>、收藏（Star）](#2%E6%94%B6%E8%97%8Fstar)
    - [<3>、复制克隆项目（Fork）](#3%E5%A4%8D%E5%88%B6%E5%85%8B%E9%9A%86%E9%A1%B9%E7%9B%AEfork)
    - [<4>、发送请求（Pull Request）](#4%E5%8F%91%E9%80%81%E8%AF%B7%E6%B1%82pull-request)
    - [<5>、关注（Watch）](#5%E5%85%B3%E6%B3%A8watch)
    - [<6>、事务卡片（Issue）](#6%E4%BA%8B%E5%8A%A1%E5%8D%A1%E7%89%87issue)
  - [(3)、主页介绍](#3%E4%B8%BB%E9%A1%B5%E4%BB%8B%E7%BB%8D)
    - [<1>、GitHub主页](#1github%E4%B8%BB%E9%A1%B5)
    - [<2>、仓库主页](#2%E4%BB%93%E5%BA%93%E4%B8%BB%E9%A1%B5)
    - [<3>、个人主页](#3%E4%B8%AA%E4%BA%BA%E4%B8%BB%E9%A1%B5)
  - [(4)、注册GitHub账号](#4%E6%B3%A8%E5%86%8Cgithub%E8%B4%A6%E5%8F%B7)
  - [(5)、使用注意](#5%E4%BD%BF%E7%94%A8%E6%B3%A8%E6%84%8F)
    - [<1>、关于网络](#1%E5%85%B3%E4%BA%8E%E7%BD%91%E7%BB%9C)
    - [<2>、关于仓库类型](#2%E5%85%B3%E4%BA%8E%E4%BB%93%E5%BA%93%E7%B1%BB%E5%9E%8B)
    - [<3>、关于邮箱](#3%E5%85%B3%E4%BA%8E%E9%82%AE%E7%AE%B1)
  - [(6)、创建仓库/创建新项目](#6%E5%88%9B%E5%BB%BA%E4%BB%93%E5%BA%93%E5%88%9B%E5%BB%BA%E6%96%B0%E9%A1%B9%E7%9B%AE)
    - [<1>、点击创建仓库、项目](#1%E7%82%B9%E5%87%BB%E5%88%9B%E5%BB%BA%E4%BB%93%E5%BA%93%E9%A1%B9%E7%9B%AE)
    - [<2>、填写仓库名（一般与项目名称一致）](#2%E5%A1%AB%E5%86%99%E4%BB%93%E5%BA%93%E5%90%8D%E4%B8%80%E8%88%AC%E4%B8%8E%E9%A1%B9%E7%9B%AE%E5%90%8D%E7%A7%B0%E4%B8%80%E8%87%B4)
    - [<3>、填写项目描述](#3%E5%A1%AB%E5%86%99%E9%A1%B9%E7%9B%AE%E6%8F%8F%E8%BF%B0)
    - [<4>、选择Public公共仓库类型](#4%E9%80%89%E6%8B%A9public%E5%85%AC%E5%85%B1%E4%BB%93%E5%BA%93%E7%B1%BB%E5%9E%8B)
    - [<5>、选择附加一个README说明文件，来详细描述项目](#5%E9%80%89%E6%8B%A9%E9%99%84%E5%8A%A0%E4%B8%80%E4%B8%AAreadme%E8%AF%B4%E6%98%8E%E6%96%87%E4%BB%B6%E6%9D%A5%E8%AF%A6%E7%BB%86%E6%8F%8F%E8%BF%B0%E9%A1%B9%E7%9B%AE)
    - [<6>、完成创建](#6%E5%AE%8C%E6%88%90%E5%88%9B%E5%BB%BA)
  - [(7)、仓库的管理与使用](#7%E4%BB%93%E5%BA%93%E7%9A%84%E7%AE%A1%E7%90%86%E4%B8%8E%E4%BD%BF%E7%94%A8)
    - [<1>、新建文件](#1%E6%96%B0%E5%BB%BA%E6%96%87%E4%BB%B6)
      - [1、填写文件名（要带扩展名）](#1%E5%A1%AB%E5%86%99%E6%96%87%E4%BB%B6%E5%90%8D%E8%A6%81%E5%B8%A6%E6%89%A9%E5%B1%95%E5%90%8D)
      - [2、填写文件内容](#2%E5%A1%AB%E5%86%99%E6%96%87%E4%BB%B6%E5%86%85%E5%AE%B9)
      - [3、填写提交的目的，方便其他开发者知道原因](#3%E5%A1%AB%E5%86%99%E6%8F%90%E4%BA%A4%E7%9A%84%E7%9B%AE%E7%9A%84%E6%96%B9%E4%BE%BF%E5%85%B6%E4%BB%96%E5%BC%80%E5%8F%91%E8%80%85%E7%9F%A5%E9%81%93%E5%8E%9F%E5%9B%A0)
      - [4、commit new file](#4commit-new-file)
    - [<2>、修改文件](#2%E4%BF%AE%E6%94%B9%E6%96%87%E4%BB%B6)
      - [1、点击文件名进入文件详情页](#1%E7%82%B9%E5%87%BB%E6%96%87%E4%BB%B6%E5%90%8D%E8%BF%9B%E5%85%A5%E6%96%87%E4%BB%B6%E8%AF%A6%E6%83%85%E9%A1%B5)
      - [2、点击Edit this file](#2%E7%82%B9%E5%87%BBedit-this-file)
    - [<3>、删除文件](#3%E5%88%A0%E9%99%A4%E6%96%87%E4%BB%B6)
      - [1、点击文件名进入文件详情页](#1%E7%82%B9%E5%87%BB%E6%96%87%E4%BB%B6%E5%90%8D%E8%BF%9B%E5%85%A5%E6%96%87%E4%BB%B6%E8%AF%A6%E6%83%85%E9%A1%B5-1)
      - [2、点击Delete this file](#2%E7%82%B9%E5%87%BBdelete-this-file)
    - [<4>、上传文件](#4%E4%B8%8A%E4%BC%A0%E6%96%87%E4%BB%B6)
      - [1、选择 Upload files](#1%E9%80%89%E6%8B%A9-upload-files)
      - [2、拖动文件或直接上传（一次可以多个文件）](#2%E6%8B%96%E5%8A%A8%E6%96%87%E4%BB%B6%E6%88%96%E7%9B%B4%E6%8E%A5%E4%B8%8A%E4%BC%A0%E4%B8%80%E6%AC%A1%E5%8F%AF%E4%BB%A5%E5%A4%9A%E4%B8%AA%E6%96%87%E4%BB%B6)
    - [<5>、搜索仓库文件](#5%E6%90%9C%E7%B4%A2%E4%BB%93%E5%BA%93%E6%96%87%E4%BB%B6)
      - [1、选择 Go to file](#1%E9%80%89%E6%8B%A9-go-to-file)
      - [2、输入文件名称进行筛选](#2%E8%BE%93%E5%85%A5%E6%96%87%E4%BB%B6%E5%90%8D%E7%A7%B0%E8%BF%9B%E8%A1%8C%E7%AD%9B%E9%80%89)
    - [<6>、下载/检出项目](#6%E4%B8%8B%E8%BD%BD%E6%A3%80%E5%87%BA%E9%A1%B9%E7%9B%AE)
  - [(8)、GitHub Issues](#8github-issues)
    - [<1>、作用](#1%E4%BD%9C%E7%94%A8)
    - [<2>、情景](#2%E6%83%85%E6%99%AF)
    - [<3>、操作步骤](#3%E6%93%8D%E4%BD%9C%E6%AD%A5%E9%AA%A4)
      - [1、点击Issues](#1%E7%82%B9%E5%87%BBissues)
      - [2、点击New issues](#2%E7%82%B9%E5%87%BBnew-issues)
      - [3、编辑内容](#3%E7%BC%96%E8%BE%91%E5%86%85%E5%AE%B9)
      - [4、开始交流](#4%E5%BC%80%E5%A7%8B%E4%BA%A4%E6%B5%81)
      - [5、完成交流关闭Issues（先交流，完成后再关闭）](#5%E5%AE%8C%E6%88%90%E4%BA%A4%E6%B5%81%E5%85%B3%E9%97%ADissues%E5%85%88%E4%BA%A4%E6%B5%81%E5%AE%8C%E6%88%90%E5%90%8E%E5%86%8D%E5%85%B3%E9%97%AD)
  - [(9)、开源项目贡献流程](#9%E5%BC%80%E6%BA%90%E9%A1%B9%E7%9B%AE%E8%B4%A1%E7%8C%AE%E6%B5%81%E7%A8%8B)
    - [<1>、新建Issue](#1%E6%96%B0%E5%BB%BAissue)
    - [<2>、Pull Request](#2pull-request)
      - [1、Fork项目](#1fork%E9%A1%B9%E7%9B%AE)
      - [2、修改自己的项目代码](#2%E4%BF%AE%E6%94%B9%E8%87%AA%E5%B7%B1%E7%9A%84%E9%A1%B9%E7%9B%AE%E4%BB%A3%E7%A0%81)
      - [3、新建Pull Request](#3%E6%96%B0%E5%BB%BApull-request)
      - [4、等待作者操作审核](#4%E7%AD%89%E5%BE%85%E4%BD%9C%E8%80%85%E6%93%8D%E4%BD%9C%E5%AE%A1%E6%A0%B8)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

---

# 一、使用GitHub

## (1)、目的

借助GitHub托管项目代码

## (2)、基本概念

### <1>、仓库（Repository）

仓库用来存放项目代码，每个项目对应一个仓库，多个开源项目则对应多个仓库

### <2>、收藏（Star）

收藏项目，方便下次查看

举例：李四看到张三的项目很喜欢，所以收藏了

### <3>、复制克隆项目（Fork）

举例：假如张三的GitHub上有一个test仓库，李四看到后觉得该仓库很好，希望可以保存在自己的GitHub中，由于张三的test仓库中带有一个fork功能，只要李四执行fork功能后，李四的GitHub账户中就会自动创建一个同名的test仓库，当然仓库会注明：forked from 张三/test仓库

注意：这两个test项目是独立存在的，并不会互相干扰！

### <4>、发送请求（Pull Request）

举例：由于克隆的仓库是独立的，所以说如果李四在test仓库中添加了东西的话，张三是看不到的，所以说李四要执行Pull Request功能并编写相应说明，然后张三GitHub主页会提示张三有一个请求待处理，待张三同意后才能合并到原来的test仓库中

### <5>、关注（Watch）

关注项目，当项目更新可以接到通知

举例：张三关注了李四的项目，李四添加项目文件，张三的GitHub主页会提示项目动态

### <6>、事务卡片（Issue）

发现代码BUG，但是目前没有成型代码，需要讨论时使用

## (3)、主页介绍

### <1>、GitHub主页

左侧主要显示用户动态以及关注用户或关注仓库的动态；右侧显示所有的git库

### <2>、仓库主页

主要显示项目信息，如：项目代码，版本，收藏/关注/fork 情况等

### <3>、个人主页

个人信息：头像、简介，关注我的人、我关注的人，我关注的git库，我的开源项目，我贡献的开源项目等信息

## (4)、注册GitHub账号

官方网站：<https://github.com/>

注意：

邮箱一定要是自己常用的！因为经常要接受邮件！

选择你的计划时：默认选择公开的免费仓库！（私有仓库要收费）

其他默认即可！

注册成功即可进入GitHub主页！

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924234544819.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


## (5)、使用注意

### <1>、关于网络

因为GitHub的服务器在国外，所以访问GitHub的速度很慢或者说直接访问不了，这时可以翻墙

### <2>、关于仓库类型

私有仓库只能自己或者指定的朋友才有权限操作（私有仓库是收费的）

### <3>、关于邮箱

新注册的用户必须验证邮箱后才可以创建git库

如果是QQ邮箱须要设置白名单才可以收到GitHub的邮件

详细步骤：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924234630852.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924234645354.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)



## (6)、创建仓库/创建新项目

### <1>、点击创建仓库、项目
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924234658268.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)



### <2>、填写仓库名（一般与项目名称一致）

### <3>、填写项目描述

### <4>、选择Public公共仓库类型

### <5>、选择附加一个README说明文件，来详细描述项目

### <6>、完成创建
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924234726963.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924234750264.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

## (7)、仓库的管理与使用

### <1>、新建文件

#### 1、填写文件名（要带扩展名）

#### 2、填写文件内容

#### 3、填写提交的目的，方便其他开发者知道原因

#### 4、commit new file
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924234820659.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924234833846.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924234845620.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020092423490145.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924234915469.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924234927834.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

### <2>、修改文件

#### 1、点击文件名进入文件详情页

#### 2、点击Edit this file

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235230282.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235252159.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235302493.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235311930.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235320403.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

### <3>、删除文件

#### 1、点击文件名进入文件详情页

#### 2、点击Delete this file

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235414913.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235423941.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235445386.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020092423545615.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

### <4>、上传文件

#### 1、选择 Upload files

#### 2、拖动文件或直接上传（一次可以多个文件）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235513769.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235524622.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235532510.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235606147.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020092423555082.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

### <5>、搜索仓库文件

#### 1、选择 Go to file

#### 2、输入文件名称进行筛选
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235646554.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235654548.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

### <6>、下载/检出项目
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235706292.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

## (8)、GitHub Issues

### <1>、作用

发现代码BUG，但是目前没有成型代码，需要讨论时用，或者使用开源项目出现问题时使用

### <2>、情景

张三发现李四开源git库，则提交了一个issue，李四隔天登录GitHub主页看到通知并和张三交流，最后关闭issue

### <3>、操作步骤

这里用一个账户给自己提交Issues进行演示（而实际中是其他人给自己提交Issues）

#### 1、点击Issues
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235721391.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

#### 2、点击New issues
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235730810.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

#### 3、编辑内容
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235744665.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

#### 4、开始交流
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235756886.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020092423581345.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235823341.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

#### 5、完成交流关闭Issues（先交流，完成后再关闭）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235903187.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235911522.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235919307.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924235927205.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

（注明：在GitHub主页可以直接看到Issues通知）

## (9)、开源项目贡献流程

### <1>、新建Issue

提交使用问题或者建议或者想法

### <2>、Pull Request

步骤：

#### 1、Fork项目

#### 2、修改自己的项目代码

#### 3、新建Pull Request 

#### 4、等待作者操作审核





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



