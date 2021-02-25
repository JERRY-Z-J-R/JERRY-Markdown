---
title: Java标识符命名规则——Java知识点补充(1)
date: 2020-12-21 15:48:55
categories:
- [Java]
tags:
- Java
- 命名规范
---

![在这里插入图片描述](https://img-blog.csdnimg.cn/20201221190150382.png)

<!--more-->

# 一、Java标识符命名规则——Java知识点补充(1)

> 原创内容，转载请注明出处！

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [一、Java标识符命名规则——Java知识点补充(1)](#%E4%B8%80java%E6%A0%87%E8%AF%86%E7%AC%A6%E5%91%BD%E5%90%8D%E8%A7%84%E5%88%99java%E7%9F%A5%E8%AF%86%E7%82%B9%E8%A1%A5%E5%85%851)
- [二、包（更好地组织类并解决相同类名问题）](#%E4%BA%8C%E5%8C%85%E6%9B%B4%E5%A5%BD%E5%9C%B0%E7%BB%84%E7%BB%87%E7%B1%BB%E5%B9%B6%E8%A7%A3%E5%86%B3%E7%9B%B8%E5%90%8C%E7%B1%BB%E5%90%8D%E9%97%AE%E9%A2%98)
- [三、类、接口（大驼峰表示法）](#%E4%B8%89%E7%B1%BB%E6%8E%A5%E5%8F%A3%E5%A4%A7%E9%A9%BC%E5%B3%B0%E8%A1%A8%E7%A4%BA%E6%B3%95)
- [四、对象、方法、变量（小驼峰表示法）](#%E5%9B%9B%E5%AF%B9%E8%B1%A1%E6%96%B9%E6%B3%95%E5%8F%98%E9%87%8F%E5%B0%8F%E9%A9%BC%E5%B3%B0%E8%A1%A8%E7%A4%BA%E6%B3%95)
- [五、常量](#%E4%BA%94%E5%B8%B8%E9%87%8F)
- [六、命名规则要求：见名知意](#%E5%85%AD%E5%91%BD%E5%90%8D%E8%A7%84%E5%88%99%E8%A6%81%E6%B1%82%E8%A7%81%E5%90%8D%E7%9F%A5%E6%84%8F)
- [七、示例：](#%E4%B8%83%E7%A4%BA%E4%BE%8B)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

---

# 二、包（更好地组织类并解决相同类名问题）
全部小写，域名反写

---

# 三、类、接口（大驼峰表示法）
第一个单词首字母大写，其余单词首字母大写

---

# 四、对象、方法、变量（小驼峰表示法）
第一个单词首字母小写，其余单词首字母大写

---

# 五、常量
全部大写，多个单词间使用_符号连接

---

# 六、命名规则要求：见名知意

---

# 七、示例：

```java
package com.jerry.java.demo;	//所在包

public class NamingTheDemo {
    public static void main(String[] args) {
        //实例化计算机专业学生对象：jerryZhou
        ComputerMajorsStudents jerryZhou = new ComputerMajorsStudents("jerryZhou", 201940, 20);
        jerryZhou.personalInformation();
        jerryZhou.programming();
        jerryZhou.playGames();
    }
}

//接口：程序员技能
interface ProgrammerSkill {
    public void programming();      //编程
    public void playGames();        //玩游戏
}

//类：计算机专业学生
class ComputerMajorsStudents implements ProgrammerSkill  {
    private String name;
    private int id;
    private int age;
    //字符串常量：大学专业
    public static final String UNIVERSITY_MAJOR = "Computer Science And Technology";

    //空参构造函数
    public ComputerMajorsStudents() {

    }

    //带参构造函数
    public ComputerMajorsStudents(String name, int id, int age) {
        this.name = name;
        this.id = id;
        this.age = age;
    }

    public String getName() {
        return name;
    }

    public int getId() {
        return id;
    }

    public int getAge() {
        return age;
    }

    public void setName(String name) {
        this.name = name;
    }

    public void setId(int id) {
        this.id = id;
    }

    public void setAge(int age) {
        this.age = age;
    }

    //个人信息
    public void personalInformation() {
        System.out.println("Name:" + name + "\nId:" + id + "\nAge:" + age + "\nUniversity major:" + UNIVERSITY_MAJOR);

    }

    //重写接口方法
    public void programming() {
        System.out.println("Coding...");
    }

    //重写接口方法
    public void playGames() {
        System.out.println("Play...");
    }
}

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

