---
title: 为什么C++很少用于Web后端开发？
date: 2020-12-01 04:00:09
categories: 
- [C++]
tags:
- C++
- Web后端
---

<img src="https://pic4.zhimg.com/50/v2-515b5b44f2bc923e1bbf9f403fc240d6_hd.jpg?source=1940ef5c" data-caption="" data-size="normal" data-rawwidth="533" data-rawheight="338" data-default-watermark-src="https://pic2.zhimg.com/50/v2-cdb0c6a5a248ada043a69119e5ba1c32_hd.jpg?source=1940ef5c" class="origin_image zh-lightbox-thumb" width="533" data-original="https://pic4.zhimg.com/v2-515b5b44f2bc923e1bbf9f403fc240d6_r.jpg?source=1940ef5c"/>

<!--more-->

# 为什么C++很少用于Web后端开发？

> 特别说明：以下内容来自知乎！

同样面向对象，为什么Web后端开发中 Java应用的很广泛，C++用的很少呢？
目前想到的可能问题有：

1. 是C++本身的语言特性问题？
2. 没有一个像Oracle一样的公司推动C++的Web开发标准指定以及相关库的开发？
3. C++学习成本太高？
4. 还是其他？

---

原因很多：相比于Java、.net、php等开发效率低太多，低到无法忍受，不符合互联网的短平快、快速迭代、灰度发布。领Web后端开发中语言本身带来的性能提升并没有那么重要，绝大多数时候系统的瓶颈在架构和数据库上，Web项目通常要敏捷开发, 好占据先机, 所以性能不是很重要(至少是前期), 更需要入门快，上手快Web需求变化多端且朝令夕改，所以性能无法顾忌， 需要更容易重构，有一定动态能力的，灵活的语言C++开发成本高，招人难， 所以只能用在刀刃上,，可在少量对性能高的地方用(很可能是直接用第三方写好的中间件)， 所以通常让人觉得主要不用C++写C++不是万能的， 也没有任何一门语言是万能的, 这一点要谨记。

> 作者：dwing
链接：https://www.zhihu.com/question/26782196/answer/975604841
来源：知乎
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

---

世界上主要的Web后端，都是用C/C++编写的比如目前谷歌、百度、腾讯、脸书、Youtube等公司的后端，主要是C++。另外一些商务型公司，则采用Java。其次，大部分互联网底层平台（操作系统、Web服务器、数据库等），编程语言、相关扩展库，也大都是C/C++开发的。参见下图，来自：https://www.mentofacturing.com/vincent/implementations.html<img src="https://pic4.zhimg.com/50/v2-e0fc5b11e571fe2aa9b4aa69678e8a22_hd.jpg?source=1940ef5c" data-caption="" data-size="normal" data-rawwidth="937" data-rawheight="524" data-default-watermark-src="https://pic4.zhimg.com/50/v2-8b67a95eacaf77cf2c10f33694e4747a_hd.jpg?source=1940ef5c" class="origin_image zh-lightbox-thumb" width="937" data-original="https://pic2.zhimg.com/v2-e0fc5b11e571fe2aa9b4aa69678e8a22_r.jpg?source=1940ef5c"/><img src="https://pic4.zhimg.com/50/v2-25befed6fe33a940cb5d9e91917eaf71_hd.jpg?source=1940ef5c" data-caption="" data-size="normal" data-rawwidth="1037" data-rawheight="914" data-default-watermark-src="https://pic2.zhimg.com/50/v2-faac0235f9bff390a4687deab4cc2cfc_hd.jpg?source=1940ef5c" class="origin_image zh-lightbox-thumb" width="1037" data-original="https://pic2.zhimg.com/v2-25befed6fe33a940cb5d9e91917eaf71_r.jpg?source=1940ef5c"/>当然，这些基础平台的开发国内很少涉及，全都是用国外C/C++程序员开发好的产品（开源或商业收费）。完全没有中国开发者参与，所以导致被完全忽视。C/C++编写的程序，占互联网后台90%以上的运算能力C/C++性能最好，但是开发效率最低。因此除了基础部件、调用频繁的库，普通网站大部分业务逻辑都会用开发效率更高的语言来编写。<img src="https://pic4.zhimg.com/50/v2-515b5b44f2bc923e1bbf9f403fc240d6_hd.jpg?source=1940ef5c" data-caption="" data-size="normal" data-rawwidth="533" data-rawheight="338" data-default-watermark-src="https://pic2.zhimg.com/50/v2-cdb0c6a5a248ada043a69119e5ba1c32_hd.jpg?source=1940ef5c" class="origin_image zh-lightbox-thumb" width="533" data-original="https://pic4.zhimg.com/v2-515b5b44f2bc923e1bbf9f403fc240d6_r.jpg?source=1940ef5c"/>C/C++占互联网后台运算能力统计：按平台算约100%：C/C++几乎包揽了全部Web后台的运算能力。操作系统、Web服务器、数据库、大部分编程语言、扩展库全都囊括在内。包括API和库调用来算占90%以上：除其他高级语言代码，C/C++占用了互联网后台90%以上的运算能力。其他低性能语言直接承载的运算较少，大部分运算是调用的C/C++编写的系统API和库。只按后端语言计算（大家常见的）：C/C++后端几大巨头在用，还有一些局部领域应用，总量确实较少，但权重有半壁江山也毫不夸张。并且通常有封装，前端直接看不到。谷歌后台内核主要是C/C++，代码量是Windows的30倍。Python运算性能比C/C++慢200倍以上，只用于周边和大数据AI的胶水语言。结果到处在误传谷歌后端用Python（来支撑大家常见的业务）。当然，Python Web服务器性能可以达到C/C++的1/10，可以承载一些负载较轻、或原型性质的业务。为什么比C++慢200多倍的Python，服务器性能却能达到C++的1/10呢？因为Python大部分时间都是在运行C编写的扩展库以及系统IO，本身py代码运力占比只有5%。<img src="https://pic2.zhimg.com/50/v2-92e8a4dc9430c6bc82f22efef629f17e_hd.jpg?source=1940ef5c" data-caption="" data-size="normal" data-rawwidth="1000" data-rawheight="192" data-default-watermark-src="https://pic2.zhimg.com/50/v2-c34273dd11d89c3b39135973a8d87e0f_hd.jpg?source=1940ef5c" class="origin_image zh-lightbox-thumb" width="1000" data-original="https://pic2.zhimg.com/v2-92e8a4dc9430c6bc82f22efef629f17e_r.jpg?source=1940ef5c"/>【这是一道小学奥数题】：已知C/C++（C、C++速度几乎相等，可忽略差异）的速度是Python的200倍。Python和C++走过同样一段路程。Python中间有乘坐C，总耗时是C++的10倍。求Python独立行走的路程占整段路程的百分比？

答案为：大约5%。

只有那些巨头网站，才有资源和能力用C++来写后台。因为海量服务器的成本差异，远远超过C++开发成本的增长。比如某服务Python要用1000万台服务器，PHP用300万台，Java用200万台，C++用100万台。肯定选C++，节省几十几百亿。比如脸书已经全面从PHP迁移到C++(70%C++和30%PHP转译C++)，服务器减少到原来的三分之一。 而Python最具盛名的网站Youtube也已迁移到C++，此前用C来优化Python依然不能满足。对于小型网站，如果Python用10台服务器、PHP用3台、Java用2台、C++用1台服务器。甚至起初任何语言一台服务器都够用。这时肯定不会选C++，因为开发成本比服务器贵的多。通常我们粗略估算C++需要两倍的开发成本，一个普通开发约30-50万总成本每年，能节省上百台服务器时才划算。而且C++直接写Web痛苦指数高、快速反应能力低、大量熟手招聘困难，需要有更大成本优势时（成千上万台服务器），才会被采用。互联网C/C++的替代品：GoC/C++入门并不难学。但因为和硬件底层更近，所以程序形态与自然语言距离更远，需要写更多行语句和花更多时间去掌握。而夺命指针，即是性能飙升的利器，也是程序崩坏的元凶。因此，C++要更多时间去编译、测试和检查程序，才能保证稳定，不适合快速开发更迭。实际上是后端开发语言太方便、灵活、稳定了，倒逼C++只能去做内核了。互联网光一般的更迭速度，C++的缓慢接近凝滞的身段，令人没法提起改进C++直接Web开发的兴趣。索性直接写出了PHP、http://ASP.NET、JSP等支持高效开发的产品。但当网站规模增大的时候，高并发和密集运算部分C/C++又成为了必须的选择。Go就是谷歌为了解决这些痛点，应运而生的。具备接近C的性能，但更安全快速、更具备互联网基因，目前在后端增长最快。

> 
> 作者：无缺草
链接：https://www.zhihu.com/question/26782196/answer/968086477?utm_source=wechat_session
来源：知乎
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

---

业务迭代效率互联网的web后端追求短平快，这里倒不是说cpp效率不高，cpp在多范式上结合了oop和fp，同时保留了c的过程式，拥有几乎所有的语言特性，因此cpp是很强大的，但也就是因为这些特性，再加上特有的pointer，reference 与之叠加起来，cpp是非常非常复杂的，所以一般的公司是很难把控cpp写出来的质量的，这点java虽然死板，但在工程上来说更可控。还有后端最重要的一个技能就是使用轮子，面向github/stackoverflow/google编程，这点java有很多顶级的后端的轮子，而cpp相对来说没有那么多，当然大厂有很多封装好的轮子，譬如google/tencent等，单对于一般的公司来说，一是没有造这种顶级轮子的实力，二是业务迭代也不允许去造，所以java、Python这种能直接import package对大多数公司来说会更合适。2. web后端的特点web后端大多数是和db以及cache打交道，操作数据的时候嵌套业务逻辑，这一特点决定了web后端是重io, 轻计算的，因此好的IO并发模型，好的缓存设计才是关键。因此语言层面带来的性能提升面对磁盘寻道可以忽略不计。

> 作者：威士忌的碎冰
链接：https://www.zhihu.com/question/26782196/answer/993217316
来源：知乎
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。


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