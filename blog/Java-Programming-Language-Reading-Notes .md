---
title: 《Java 语言程序设计》—— 读书笔记
date: 2021-03-11 13:00:09
categories:
- [Java]
- [读书笔记]
tags:
- Java
- 读书笔记
- 《Java 语言程序设计》
cover: https://img-blog.csdnimg.cn/20210311232236882.jpg
---

# 《Java 语言程序设计》—— 读书笔记

**《全国计算机等级考试 二级教程 教育部考试中心（2021 年版）Java 语言程序设计》**

> 原创内容，转载请注明出处！

> 笔记只是对本书部分内容的归纳，并不涉及全部内容。

# 一、递归

本质：自己调用自己（直接或间接）。

优点：通过简洁直观的方式解决复杂的规律性问题。

缺点：深度的递归会占用大量的系统堆栈，内存消耗越多，其运算速度与循环相比也要慢得多。

结构：

- **定义递归头**：递归结束的标志（跳出递归的判断语句）。
- **定义如何从同性质的简化问题求得当前问题**：用不同的参数（体现范围缩小）来调用递归方法自身。例如求 n! 这个问题被划分为求 `n * (n-1)!`，同理 `(n-1)!` 又划分为 `(n-1) * (n-2)!` …… 所以，`输出值 = 输入值 * (输入值-1)!` 

举例：利用递归结构求 n!

```java
import java.util.Scanner;

public class FactorialTest {
    static long factorial(int n) {			// 定义静态求阶乘函数（可直接使用）
        if (n == 1) {						// 递归头
            return 1;
        } else {
            return n * factorial(n - 1);	// 递归调用自身
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        System.out.print("please enter n: ");
        int n = sc.nextInt();
        
        System.out.println(n + "! = " + factorial(n));
    }
}
```

# 二、枚举

```java
import java.util.Scanner;

public class Test {
    enum Size {
        SMALL("S"),
        MEDIUM("M"),
        LARGE("L"),
        EXTRA_LARGE("XL"),
        EXTRA_EXTRA_LARGE("XXL");

        private String abbreviation;

        private Size(String abbreviation) {
            this.abbreviation = abbreviation;
        }

        public String getAbbreviation() {
            return abbreviation;
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("please enter size: (SMALL, MEDIUM, LARGE, EXTRA_LARGE, EXTRA_EXTRA_LARGE)");
        String input = sc.next().toUpperCase();

        Size size = Enum.valueOf(Size.class, input);
        // Size size = Size.valueOf(input);

        System.out.println("size = " + size);
        System.out.println("abbreviation = " + size.getAbbreviation());

        if (size == Size.EXTRA_LARGE ^ size == Size.EXTRA_EXTRA_LARGE) {
            System.out.println("you well! You noticed the '_'underscore.");
        }
    }
}
```



# 三、异常与断言

# 四、输入输出及文件操作

# 五、线程

# 六、编写图形用户界面

## 6.1 概述

Java GUI 技术经历了两个发展阶段：`AWT` 开发包 ——> `Swing` 开发包。

核心思想：组件化。

三个重要问题：

- 组件的放置
- 组件响应用户操作
- 组件的显示效果

## 6.2 AWT 编写 GUI

AWT：抽象窗口工具包。

### 6.2.1 java.awt 包

提供了基本 GUI 设计工具，主要包括：组件（Component）、容器（Container）、布局管理器（LayoutManager）三个概念，每个概念对应一个类。

### 6.2.2 组件、容器、布局管理器

**组件（Component）：**

- GUI 最基本元素
- 图形化方式显示并能与用户交互的对象
- 不能独立显示、必须放在容器中

java.awt.Component 是许多组件类的父类，其子类如下：
- Container
  - Panel
    - Applet
  - Window
    - Frame

实际开发中一般都是使用其子类，由于 Component 类中封装了组件通用的方法和属性，因此其组件子类也继承了这些成员方法和成员变量，比如：

```java
getComponentAt(int x, int y)	// 获得坐标（x, y）上的组件对象
getFont()						// 获得组件的字体
getForeground()					// 获得组件的前景色
getName() 						// 获得组件的名字
getSize()						// 获得组件的大小
paint(Graphics g)				// 绘制组件
repaint()						// 重新绘制组件
setVisible(Boolean b)			// 设置组件是否可见
setSize(Dimension d)			// 设置组件的大小
setName(String name)			// 设置组件的名字
```

**容器（Container）：**

容器 Container 是一个类，实际上是 Component 的子类，因此容器本质上也是一个组件，具有组件的所有性质，但是其主要功能在于放置其他组件和容器，在实际开发中，往往采用的都是容器类 Container 的子类。

**布局管理器（LayoutManager）：**

- 用于管理组件放置在容器中的位置和大小
- 每个容器都有一个布局管理器
- LayoutManager 是一个接口，实际开发中通常使用的是实现了该接口的类

注意：

- 在布局管理器负责组件的时候，无法手动设置这些组件的属性，如：`setLocation()`、`setSize()`、`setBounds()` 等方法将会被布局管理器覆盖。
- 如果需要亲自手动设置组件，则应取消该容器的布局管理器，方法为：`setLayout(null)`；然后再调用 `setLocation()`、`setSize()`、`setBounds()` 等方法。

### 6.2.3 常用容器

容器可以

# 七、Applet 程序设计

# 八、集合与泛型

# 九、JDK 操作命令及 Java 编程规范

