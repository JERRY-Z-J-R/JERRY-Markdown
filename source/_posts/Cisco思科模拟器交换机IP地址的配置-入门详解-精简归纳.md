---
title: Cisco思科模拟器交换机IP地址的配置 入门详解 - 精简归纳
date: 2020-10-11 21:21:01
categories:
- [个人教程]
- [计算机网络]
tags:
- Cisco
- 交换机
- IP
---

![在这里插入图片描述](https://img-blog.csdnimg.cn/2020101118401779.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

<!--more-->



# Cisco思科模拟器 交换机IP地址的配置 入门详解 - 精简归纳

> 原创内容，转载请注明出处！

---

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Cisco思科模拟器 交换机IP地址的配置 入门详解 - 精简归纳](#cisco%E6%80%9D%E7%A7%91%E6%A8%A1%E6%8B%9F%E5%99%A8-%E4%BA%A4%E6%8D%A2%E6%9C%BAip%E5%9C%B0%E5%9D%80%E7%9A%84%E9%85%8D%E7%BD%AE-%E5%85%A5%E9%97%A8%E8%AF%A6%E8%A7%A3---%E7%B2%BE%E7%AE%80%E5%BD%92%E7%BA%B3)
- [一、IP地址基本概念](#%E4%B8%80ip%E5%9C%B0%E5%9D%80%E5%9F%BA%E6%9C%AC%E6%A6%82%E5%BF%B5)
- [二、十进制与二进制的快速转换（凑权法）](#%E4%BA%8C%E5%8D%81%E8%BF%9B%E5%88%B6%E4%B8%8E%E4%BA%8C%E8%BF%9B%E5%88%B6%E7%9A%84%E5%BF%AB%E9%80%9F%E8%BD%AC%E6%8D%A2%E5%87%91%E6%9D%83%E6%B3%95)
- [三、选择交换机与主机并连接](#%E4%B8%89%E9%80%89%E6%8B%A9%E4%BA%A4%E6%8D%A2%E6%9C%BA%E4%B8%8E%E4%B8%BB%E6%9C%BA%E5%B9%B6%E8%BF%9E%E6%8E%A5)
- [四、配置主机](#%E5%9B%9B%E9%85%8D%E7%BD%AE%E4%B8%BB%E6%9C%BA)
- [五、命令配置交换机](#%E4%BA%94%E5%91%BD%E4%BB%A4%E9%85%8D%E7%BD%AE%E4%BA%A4%E6%8D%A2%E6%9C%BA)
- [六、检测](#%E5%85%AD%E6%A3%80%E6%B5%8B)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

---

# 一、IP地址基本概念
IP地址通俗的解释：唯一识别一台主机的标记
（IP地址是一个32位的标记符，如：192.168.1.1）
（lpv4标准：32位，lpv6标准：128位）

---

# 二、十进制与二进制的快速转换（凑权法）
2^0^ = 1
2^1^ = 2
2^2^ = 4
2^3^ = 8
2^4^ = 16
2^5^ = 32
2^6^ = 68
2^7^ = 128
2^8^ = 256
2^9^ = 512
2^10^ = 1024
2^11^ = 2048

转换方法举例：

2049 = 2048 + 1：
1000 0000 0000 + 1 = 1000 0000 0001

259 = 256 + 3 = 256 + 2 + 1:
100000000 + 10 + 1 = 1 0000 0011 (0001 0000 0011)

1023 = 1024 - 1:
1000 0000 0000 - 1 = 011 1111 1111 (0011 1111 1111)

---

# 三、选择交换机与主机并连接
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201011183340875.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020101118401779.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020101118515180.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201011185212817.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201011185231832.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


---

# 四、配置主机
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020101118532092.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201011185342130.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

---

# 五、命令配置交换机
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201011185443770.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201011185501559.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201011185522946.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020101118560726.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201011185623431.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201011185656569.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201011185717235.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201011185735914.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201011185758286.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)

---

# 六、检测
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201011185822810.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201011185903652.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201011185943554.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201011185959693.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0Rfc2lfR29k,size_16,color_FFFFFF,t_70#pic_center)


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