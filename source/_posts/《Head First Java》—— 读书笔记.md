---
title: 《Head First Java》—— 读书笔记
date: 2021-02-24 13:51:41
categories:
- [Java]
- [读书笔记]
tags:
- Java
- 读书笔记
- 《Head First Java》
---

![在这里插入图片描述](https://img-blog.csdnimg.cn/20210224151452149.jpg)

<!-- more -->

# 《Head First Java》—— 知识点归纳

> 此篇为博主《Head First Java》的读书笔记
>
> 原创内容，学习不易，转载请注明出处，感谢！

<!-- toc -->

> 感谢 《Head First Java》!

# 前言：学习需求

## 一、所需工具

- 一个文本编辑器（目前不推荐使用 `IDE` “集成开发环境”，推荐 `Sublime Test` 或 `VSCode`）
- 一个终端命令行（使用命令列有利于真正地理解内部运作）
- 一个浏览器（推荐 `Chrome` 不要问为什么）
- 一个音乐播放器（不关书的事，是老子推荐的！）
- JDK API 文档（非常重要！！！）

## 二、Java 的安装与配置

1. 需要 `1.5` 版本以上的 `Java SDK` 即：`JDK` （推荐 `1.8` 版本不要问为什么），请从 [Oracle 官网](https://www.oracle.com/cn/index.html) 获取。（Java 原本属于 Sun 公司，后来被 Oracle 收购）
2. 找到 `jdk/bin` 目录，并将其 `绝对路径` 添加到 `PATH` 系统环境变量中。原因是：该目录下存放有 `javac.exe` `java.exe` 及其他重要工具，放到 PATH 中后，在终端输入 `javac` `java` 等指令时，系统便会知道要去哪里找到并运行对应的工具。

## 三、说明

- 书中的首要目标是让读者学习 Java 的基本概念，然后才是开发 Java 过程的组织与管理动作的细节，这些细节在真实环境中非常重要，所以我们会很深入地讨论，但是组织管理细节被安排在后面的章节中。
- 本书的主要内容较为基础，距离实际的开发还有很大的距离，博主在归纳本书的内容时会省略一些基本的概念及原理的介绍，有关 Java 基本语法的内容请参考我另外的文章，此篇的主要目的在于归纳《Head First Java》中所出现的一些非基础语法概念，同时在阅读《Head First Java》后推荐您阅读《Java 核心技术 卷1》及《Java 编程思想》这两本 Java 圣经，有空的话请再阅读下《Head First 设计模式》不要问为什么……

# 第一章：进入 Java 的世界——基本概念

## 一、Java 的工作方式

### 1.1 基本步骤

1. 编写 `.java` 源代码。

2. 执行 `javac` 命令 运行 `javac.exe` Java 编译器 对 `.java` 源文件进行编译 并生成同名 `.class` 字节码文件。 
3. 执行 `java` 命令 运行 `java.exe` Java 解释器 启动 `JVM` Java 虚拟机 来运行 `.class` 文件，JVM 会将字节码文件转换成当前平台能够理解的形式来运行，这也是 Java 语言跨平台特性的基础。

### 1.2 案例

1. 编写 `Hello.java` 源代码

```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}
```

2. 终端当前路径下执行 `javac` 命令

``` 
javac Hello.java		（若执行成功，则会在当前目录下生成一个 Hello.class 文件）
```

3. 终端当前路径下执行 `java` 命令

```
java Hello				（若执行成功，则会在终端窗口打印 Hello World!）
```




