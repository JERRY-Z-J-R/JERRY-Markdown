---
title: Go的第一个Hello程序 简简单单 - 快快乐乐
date: 2020-12-01 14:00:01
categories:
- [个人教程]
- [Go]
tags:
- Go
---


![封面](https://img-blog.csdnimg.cn/20201029224737965.jpg)

<!--more-->

# Go的第一个Hello程序 简简单单 - 快快乐乐

> 原创内容，转载请注明出处！

---

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Go的第一个Hello程序 简简单单 - 快快乐乐](#go%E7%9A%84%E7%AC%AC%E4%B8%80%E4%B8%AAhello%E7%A8%8B%E5%BA%8F-%E7%AE%80%E7%AE%80%E5%8D%95%E5%8D%95---%E5%BF%AB%E5%BF%AB%E4%B9%90%E4%B9%90)
- [一、Go程序开发基本结构](#%E4%B8%80go%E7%A8%8B%E5%BA%8F%E5%BC%80%E5%8F%91%E5%9F%BA%E6%9C%AC%E7%BB%93%E6%9E%84)
- [二、利用VSCode编写并在终端编译运行](#%E4%BA%8C%E5%88%A9%E7%94%A8vscode%E7%BC%96%E5%86%99%E5%B9%B6%E5%9C%A8%E7%BB%88%E7%AB%AF%E7%BC%96%E8%AF%91%E8%BF%90%E8%A1%8C)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


---
# 一、Go程序开发基本结构
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029224637808.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029224647893.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029224654672.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029224701710.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029224707840.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029224723920.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

---


# 二、利用VSCode编写并在终端编译运行
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201029224737965.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
```go
/*
** JERRY_Z 2020/10/29
*/

package main		//表示该.go文件在main这个包中，go文件都必须归属于一个包中
import "fmt"		//表示导入fmt这个包，导入这个包后就可以使用该包内的函数

func main() {		//func是一个关键字，表示这是一个函数，main为函数名，main为主函数，即程序的入口
	fmt.Println("Hello,World! Hello,Go!")		//调用fmt包中的Println函数，用于输出
}
```

```cmd
go bulid x.go   //编译.go文件（编译成功后生成同名.exe文件）
x.exe			//运行.exe文件

go run x.go		//编译.go文件并运行.exe文件（不推荐）
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