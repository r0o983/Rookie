# Python基础01--Python的介绍

## 基本概念

Python是一种高层次的,解释性的,交互式和面向对象的脚本语言.Python被设计成具有很强的可读性,它使用英语如其他语言重用空白作为标点符号,它比其他语言
语法结构更少  
Python is a high-level, interpretive, interactive and object-oriented scripting language. Python is designed to be highly 
readable,it uses English like other languages to reuse whitespace as punctuation and it has a better syntx than other 
languages less structure

## 实际练习
在本章节中首先展示如何进行输出(打印)一行语句(命令)
![打印](https://www.z4a.net/images/2020/03/30/ex01-0.png)
在实际操作中只需要调用系统内置函数来进行输出即可.  
In actual operation you only need to call the built-in function of the system for output  
print()函数  
print() function

实际效果：  
![打印1](https://www.z4a.net/images/2020/03/30/ex01-1.png)

## 分析与总结
在本章节中只调用了一个print()函数. 该内置函数在python文档中注解如下:  
only one print() function is called in this section This built-in function is annotated in the python documentation as follows:

![打印2](https://www.z4a.net/images/2020/03/30/ex01-3.png)
在脚本编写的过程中要注意引号的使用.(代码块中的引号都要成对出现)以及代码中存在中文编码的问题.  
Pay attention to the use of quotation marks in the script writing process (the quotation marks in the code block must appear
in pairs) and the problem of Chinese encoding in the code  
中文编码问题解决方式如下:  
在代码的头部代码块中添加#-*- coding:utf-8 -*- 即可解决中文编码问题  
The Chinese coding problem is solved as follows:  
Add #-*- coding:utf-8 -*- to the code block at the head of the code to solve the Chinese coding problem

## 附加练习
### 练习1尝试让脚本多输出一行
#### 简述答案：
直接使用print()语句输出一个空行即可，或者在当前输出语句后直接跟上\n即可  
Just use the print(0 statement to output a blank line, or just follow the \n immediately after the current output statement.
### 脚本
![打印4](https://www.z4a.net/images/2020/03/30/ex01-4.png)  
结果:  
![打印5](https://www.z4a.net/images/2020/03/30/ex01-5.png)  
