---
title: EditPlus配置Java环境 入门详解 - 精简归纳
date: 2020-09-17 09:36:00
categories: 
- [个人教程]
- [Java]
tags:
- EditPlus
- Java
---

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200917231001677.png)

<!--more-->

# EditPlus配置Java环境 入门详解 - 精简归纳

---

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [EditPlus配置Java环境 入门详解 - 精简归纳](#editplus%E9%85%8D%E7%BD%AEjava%E7%8E%AF%E5%A2%83-%E5%85%A5%E9%97%A8%E8%AF%A6%E8%A7%A3---%E7%B2%BE%E7%AE%80%E5%BD%92%E7%BA%B3)
- [一、EditPlus简介](#%E4%B8%80editplus%E7%AE%80%E4%BB%8B)
- [二、EditPlus-JAVA的配置](#%E4%BA%8Ceditplus-java%E7%9A%84%E9%85%8D%E7%BD%AE)
- [三、EditPlus-JAVA风格代码设置](#%E4%B8%89editplus-java%E9%A3%8E%E6%A0%BC%E4%BB%A3%E7%A0%81%E8%AE%BE%E7%BD%AE)
- [四、修改EditPlus黑暗主题](#%E5%9B%9B%E4%BF%AE%E6%94%B9editplus%E9%BB%91%E6%9A%97%E4%B8%BB%E9%A2%98)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

---
# 一、EditPlus简介
EditPlus是一款超级轻量级的编辑器，通过配置JAVA环境后，可以实现JAVA程序的编辑、编译、运行……

---

# 二、EditPlus-JAVA的配置
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020091723065939.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020091723073063.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200917230829865.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200917230808338.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200917230845727.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200917230856616.png#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200917230911516.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200917230925977.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200917230937201.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200917230948185.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200917231001677.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
至此JAVA环境遍配置好了
当然，此种方式不能提供键盘输入的功能，若需要提供键盘输入的功能，那么我们应该在Java运行配置时将动作设为：无

当然还有另外一种方法：
创建一个tool_u.ini
将该文件放入EditPlus安装包中即可！
文件内容：
```

[Tools\0]
Count=2
Text=Java编译运行
[Tools\0\0]
Text=Java编译
Command=javac
Argument=$(FileName)
InitDir=$(FileDir)
Action=1
[Tools\0\1]
Text=Java运行
Command=java
Argument=$(FileNameNoExt)
InitDir=$(FileDir)
Action=1
```

---

# 三、EditPlus-JAVA风格代码设置
由于EditPlus默认的代码风格式C语言风格，即：'{' 默认换行
而JAVA风格为 ' {' 默认不换行

设置方法：

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200917234120980.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

 修改前花括号，并保存文件![在这里插入图片描述](https://img-blog.csdnimg.cn/20200917234134882.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)![在这里插入图片描述](https://img-blog.csdnimg.cn/20200917234146834.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

 修改前花括号，并保存文件
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200917234159694.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

---

# 四、修改EditPlus黑暗主题
原本的默认主题是白色的，长时间观看会导致眼部疲劳，所以我们将其改位暗色主题，也就是上述截图中的主题
在EditPlus安装文件夹中找到editplus_u.ini
复制粘贴：

```
[Options]
Placement=2C0000000000000001000000FFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF4E0000004E0000000E0400006A020000FF
Window List=00000000000000000000000000000000FF
Marker List=00000000000000000000000000000000FF
Function List=00000000000000000000000000000000FF
Open Remote=00000000000000000000000000000000FF
Expand=00000000000000000000000000000000FF
Project Pos=00000000000000000000000000000000FF
Workspace Path=D:\APP\Editplus\anzhuangbao
Cliptext Window=145
Cliptext Window 2=452
Output=136
Output 2=170
Folding=1
Cliptext=2
Custom colors=6D6D7200FFFFFF00FFFFFF00FFFFFF00FFFFFF00FFFFFF00FFFFFF00FFFFFF0031282700FFFFFF00FFFFFF00FFFFFF00FFFFFF00FFFFFF00FFFFFF00FFFFFF00FF
Matching Brace=1
Indent guide=1
[Files]
Encoding=65001
Backup=0
Backup Remote=0
[Fonts]
Edit Window=F0FFFFFF00000000000000000000000090010000000000000302013143006F007500720069006500720020004E0065007700000000000000000000000000000000000000000000000000000000000000000000000000000000000000FF
Printer=F4FFFFFF00000000000000000000000090010000000000000000003143006F007500720069006500720020004E0065007700000000000000000000000000000000000000000000000000000000000000000000000000000000000000FF
Output Window=F4FFFFFF00000000000000000000000090010000000000000000003143006F007500720069006500720020004E0065007700000000000000000000000000000000000000000000000000000000000000000000000000000000000000FF
Cliptext Window=F4FFFFFF0000000000000000000000009001000000000001000000004D006900630072006F0073006F006600740020005900610048006500690020005500490000000000000000000000000000000000000000000000000000000000FF
Document Selector=F4FFFFFF0000000000000000000000009001000000000001000000004D006900630072006F0073006F006600740020005900610048006500690020005500490000000000000000000000000000000000000000000000000000000000FF
Hex Viewer=F4FFFFFF00000000000000000000000090010000000000010000003143006F007500720069006500720020004E0065007700000000000000000000000000000000000000000000000000000000000000000000000000000000000000FF
Custom 1=F4FFFFFF00000000000000000000000090010000000000000000002241007200690061006C000000720020004E0065007700000000000000000000000000000000000000000000000000000000000000000000000000000000000000FF
Custom 2=F5FFFFFF000000000000000000000000900100000000000000000022560065007200640061006E00610000004E0065007700000000000000000000000000000000000000000000000000000000000000000000000000000000000000FF
Custom 3=F4FFFFFF000000000000000000000000900100000000000000000012540069006D006500730020004E0065007700200052006F006D0061006E0000000000000000000000000000000000000000000000000000000000000000000000FF
Custom 4=F5FFFFFF0000000000000000000000009001000000000000000000224D0053002000530061006E0073002000530065007200690066000000000000000000000000000000000000000000000000000000000000000000000000000000FF
Custom 5=F3FFFFFF00000000000000000000000090010000000000FF000000315400650072006D0069006E0061006C00000065007700000000000000000000000000000000000000000000000000000000000000000000000000000000000000FF
[Tool Option]
Top Selector=1
[Colors\Text]
Background=2238503
Default=0
Foreground=16777215
[Colors\Keyword 1]
Foreground=8272368
Default=0
[Colors\Embedded script]
Foreground=16777215
Default=0
[Colors\Keyword 3]
Foreground=16777215
Default=0
[Colors\Keyword 6]
Foreground=8716287
Default=0
[Colors\Keyword 7]
Foreground=8716287
Default=0
[Colors\Keyword 8]
Foreground=8716287
Default=0
[Colors\Keyword 9]
Foreground=8454143
Default=0
[Colors\Keyword 10]
Foreground=8716287
Default=0
[Colors\Quotation]
Foreground=8454143
Default=0
[Colors\Quotation 2]
Foreground=5107956
Default=0
[Colors\Line comment]
Foreground=10789024
Default=0
[Colors\Line number]
Foreground=12632256
Background=2238503
Default=0
[Colors\Folding mark -]
Background=2238503
Default=0
[Colors\Matching words]
Default=0
Background=718314
[Colors\Keyword 2]
Foreground=16379142
Default=0
[Colors\Folding mark +]
Background=2238503
Default=0
[Colors\Text selection]
Background=7039851
Default=0
[Colors\Number]
Foreground=16524240
Default=0
[Colors\Block comment]
Foreground=8421504
Default=0
[Colors\Keyword 5]
Foreground=15574913
Default=0
[Colors\Ruler]
Foreground=12632256
Default=0
Background=2566187
[Colors\Cursor indicator]
Background=16777215
Default=0
[Colors\Indent Guide]
Foreground=7499117
Default=0
```


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



