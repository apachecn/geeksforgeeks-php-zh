# PHP 中的 echo、print、print_r 有什么区别？

> 原文:[https://www . geeksforgeeks . org/echo-print 和-print_r-in-php/](https://www.geeksforgeeks.org/what-is-the-difference-between-echo-print-and-print_r-in-php/) 的区别是什么

**回声:**回声不是一种功能，而是一种语言结构。它接受参数列表(可以传递多个参数)，不返回值或返回 void。它不能在 PHP 中用作变量函数。它用于显示传递给它的参数输出。它显示由逗号分隔的一个或多个字符串的输出。

**示例:**

```
<?php

// PHP program to illustrate echo

// Declare variable and initialize it.
$x = "GeeksforGeeks ";
$y = "Computer science portal";

// Display the value of $x
echo $x, $y;
?>
```

**Output:**

```
GeeksforGeeks Computer science portal

```

**打印:**不是实函数。它是一个语言构造，但总是返回值 1。所以可以作为一种表达。与 echo 不同，print 一次只接受一个参数。它不能在 PHP 中用作变量函数。打印只输出字符串。它比回声慢。
T3】例:

```
<?php

// PHP program to illustrate echo

// Declare variable and initialize it.
$x = "GeeksforGeeks";

// Display the value of $x
print $x;
?>
```

**Output:**

```
GeeksforGeeks

```