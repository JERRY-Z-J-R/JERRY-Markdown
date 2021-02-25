---
title: Sublime Text3 for Java 编译运行环境配置 入门详解 - 精简归纳
date: 2020-09-24 09:36:24
categories: 
- [个人教程]
- [Java]
tags:
- Java
- Sublime Text3
---

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924002612608.png)

<!--more-->

# Sublime Text3 for Java 编译运行环境配置 入门详解 - 精简归纳


---

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Sublime Text3 for Java 编译运行环境配置 入门详解 - 精简归纳](#sublime-text3-for-java-%E7%BC%96%E8%AF%91%E8%BF%90%E8%A1%8C%E7%8E%AF%E5%A2%83%E9%85%8D%E7%BD%AE-%E5%85%A5%E9%97%A8%E8%AF%A6%E8%A7%A3---%E7%B2%BE%E7%AE%80%E5%BD%92%E7%BA%B3)
- [一、打开用户配置文件夹](#%E4%B8%80%E6%89%93%E5%BC%80%E7%94%A8%E6%88%B7%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6%E5%A4%B9)
- [二、配置Java环境](#%E4%BA%8C%E9%85%8D%E7%BD%AEjava%E7%8E%AF%E5%A2%83)
- [三、编译JavaC](#%E4%B8%89%E7%BC%96%E8%AF%91javac)
- [四、运行JavaC - Run](#%E5%9B%9B%E8%BF%90%E8%A1%8Cjavac---run)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

---

# 一、打开用户配置文件夹
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924002119169.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924002130864.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

---

# 二、配置Java环境
编写一个 JavaC.sublime-build 文件放入User中
```
{
"cmd": ["javac","-encoding","UTF-8","-d",".","$file"],
"file_regex": "^(...*?):([0-9]*):?([0-9]*)",
"selector": "source.java",
"encoding":"GBK",
//执行完上面的命令就结束
// 下面的命令需要按Ctrl+Shift+b来运行
"variants":
    [
        {
            "name": "Run",
            "shell": true,
            "cmd" :  ["start","cmd","/c", "java ${file_base_name} &echo. & pause"],
            // /c是执行完命令后关闭cmd窗口,
            // /k是执行完命令后不关闭cmd窗口。
            // echo. 相当于输入一个回车
            // pause命令使cmd窗口按任意键后才关闭
            "working_dir": "${file_path}",
            "encoding":"GBK"
        }
    ]
}

```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924002353449.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

---

# 三、编译JavaC
Shift + Ctrl + B

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924002442525.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924002519737.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

---

# 四、运行JavaC - Run
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924002604102.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200924002612608.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)



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



