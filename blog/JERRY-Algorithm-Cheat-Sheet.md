---
title: 《JERRY 算法小抄》
date: 2021-03-07 14:27:12
categories:
- [算法]
tags:
- 算法
- 基本常用算法
cover: https://img-blog.csdnimg.cn/20210307143758493.jpg
sticky: 24
---

# 《JERRY 算法小抄》

> 原创内容，转载请注明出处！

# 【输出任意整数的绝对值】

```c
#include <stdio.h>

int main()
{
    int num;
    
    printf("Please enter num: ");
    scanf("%d", &num);
    
    if (num >= 0) {
        printf("%d\n", num);
    } else {
        printf("%d\n", num * -1);
    }
    
    return 0;
}
```

# 【输出任意正整数的位数】

```c
#include <stdio.h>

int main()
{
    int num;

    printf("Please enter num: ");
    scanf("%d", &num);
    
    int i;
    
    for (n = 0; num >= 1; n++) {
        num = num / 10;
    }
    
    printf("num is %d digits.\n", n);
    
    return 0;
}
```

# 【输出任意正整数的每一位值】

```c
// 版本1：逆序输出各位数字（从低位到高位）
#include <stdio.h>

int main()
{
    int num, temp;

    printf("Please enter num: ");
    scanf("%d", &num);
    // 将 num 赋值给临时变量 temp
    temp = num;
    
    int n;
    
    for (n = 0; temp >= 1; n++) {
        temp = temp / 10;
    }
    
    // 输出正整数的位数
    printf("num is %d digits.\n", n);

    // ---------------------------------

    // 逆序输出各位数字（从低位到高位）
    printf("The reverse order output is: ");	

    int i;
    
    for (i = n; i > 0; i--) {
        printf("%d ", num % 10);
        num = num / 10;
    }
    
    return 0;
}
```

```c
// 版本2：正序输出各位数字（从高位到低位）
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int num, temp;

    printf("Please enter num: ");
    scanf("%d", &num);
    // 将 num 赋值给临时变量 temp
    temp = num;
    
    int n;
    
    for (n = 0; temp >= 1; n++) {
        temp = temp / 10;
    }
    
    // 输出正整数的位数
    printf("num is %d digits.\n", n);

    // ---------------------------------
   
    // 定义一个 n 个空间的一维动态数组
    int arrLen = n;		// 数组长度
    int *array;			// 数组指针
    int i;				// 数组下标
    
    // 动态分配内存空间，如果失败就退出程序
    array = (int *)malloc(arrLen * sizeof(int));
    
    if (!array) {
        printf("Error: Failed to create array!\n");
        exit(1);
    }
    
    // 向内存中写入数据
    for (i = arrLen - 1; i >= 0; i--){
    	array[i] = num % 10;
        num = num / 10;
    }
        
    
    // 正序输出各位数字（从高位到低位）
    printf("The Positive order output is: ");	

    // 循环输出数组元素
    for (i = 0; i < arrLen; i++){
        printf("%d  ", array[i]);
    }
    
    // 及时释放内存空间防止内存泄漏
    free(array);
    
    return 0;
}
```

```c
// 版本3 正序输出各位数字（从高位到低位）
#include <stdio.h>
#include <math.h>

int getDigits(int num);
void printResult(int num, int n);

int main(void)
{
	int num;	// 待处理值

	printf("Please enter a num:");
	scanf("%d", &num);

	int n;	// num 的位数

	n = getDigits(num);		// 获取 num 的位数

	printf("num is %d digits.\n", n);
	
	// 正序输出各位数字（从高位到低位）
    printf("The Positive order output is: ");

	printResult(num, n);		// 输出最终结果

	return 0;
}// main

int getDigits(int num)
{
	int i;

	for (i = 1; num >= 10; ++i) {
		num /= 10;
	}

	return i;
}// getDigits

void printResult(int num, int n)
{
    int a;
    
	for (a = 0 ; n >= 1; n--) {
		a = pow(10, n - 1);		// pow 求次方数, pow(a, x): a 的 x 次方值
		printf("%d ", (num / a) % 10);	
	}// for 

}// printResult
```



# 【输出任意实数的整数及小数部分】

```c
#include <stdio.h>

int main()
{
    double num;
    
    printf("Please enter num: ");
    scanf("%lf", &num);
    
    int num_integer = (int)num;
    
    double num_decimal = num - (double)num_integer;
    
    printf("Integer is %d, Decimal is %lf\n", num_integer, num_decimal);
    
    return 0;
}
```





