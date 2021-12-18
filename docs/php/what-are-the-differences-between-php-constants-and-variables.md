# PHP 常量和变量有什么区别？

> 原文:[https://www . geesforgeks . org/PHP 常量和变量的区别是什么/](https://www.geeksforgeeks.org/what-are-the-differences-between-php-constants-and-variables/)

[**【PHP 常量】**](https://www.geeksforgeeks.org/php-constants/) **:** PHP 常量是保持不变的标识符。通常，它在脚本执行期间不会改变。它们区分大小写。默认情况下，常量标识符总是大写。通常，常数名称以下划线或字母开头，后面跟着一些字母和数字。他们不需要用$符号写常量。**常量()**函数用于返回常量的值。

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
   define("Hello", "Welcome to geeksforgeeks.com!");
   echo Hello;
?>
```

**输出:**

```
Welcome to geeksforgeeks.com!
```

[**PHP 变量:**](https://www.geeksforgeeks.org/php-variables/)**PHP 变量是赋予保存数据的内存地址的名称。声明一个 PHP 变量的基本方法是使用一个$符号，后跟变量名。一个变量帮助 PHP 代码在程序中间存储信息。如果我们在赋值前使用一个变量，那么它已经存储了一个默认值。我们可以用来构造变量的一些数据类型是整数、双精度和布尔。**

****示例:****

## **服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**

```
<?php
   $txt = "Hello from geeksforgeeks!";
   $x = 5;
   $y = 10.5;
   echo $txt;
   echo "<br>";
   echo $x;
   echo "<br>";
   echo $y;
?>
```

****输出:****

```
Hello from geeksforgeeks!
5
10.5
```

****PHP 常量与 PHP 变量的区别****

<figure class="table"> **| **PHP constant** | **PHP variable** |
| There is no need to use the $ sign in PHP constants. | The $ sign is used in PHP variables. |
| 在执行脚本的过程中，PHP 常量的数据类型不能改变。 | PHP 变量的数据类型可以在脚本的执行过程中进行更改。 |
| Once a PHP constant is defined, it cannot be redefined. | A PHP variable can be undefined or redefined. |
| 我们不能用任何简单的赋值运算符来定义一个常量，而只能用 define()来定义。 | We can use a simple assignment operation (=) to define a variable. |
| Usually, constants are written in numbers. | On the other hand, variables are written in letters and symbols. |
| PHP constants are automatically global throughout the script. | PHP variables are not automatically globalized throughout the script. |
| PHP constant is more important than PHP variable | Slow down. |** </figure>