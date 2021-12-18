# 如何在 PHP 中查找字符串中的字符数？

> 原文:[https://www . geeksforgeeks . org/如何查找 php 字符串中的字符数/](https://www.geeksforgeeks.org/how-to-find-number-of-characters-in-a-string-in-php/)

我们给了一个字符串，任务是在 PHP 中统计一个字符串中的字符数**字符串**的字符数。为了完成这个任务，我们在 PHP 中有以下方法:

**方法 1:使用** [**strlen()方法**](https://www.geeksforgeeks.org/php-strlen-function/) **:** 使用 **strlen()** 方法获取给定字符串的长度 **字符串**。L 字符串的长度，包括该方法中的所有空格和特殊字符。

**语法** :

```
strlen( $string )

```

**示例:**

## PHP

```
<?php
// PHP program to count all
// characters in a string 

$str = "  Geeks for Geeks  "; 

// Using strlen() function to
// get the length of string
$len = strlen($str);

// Printing the result
echo $len; 
?>
```

**输出**

```
19
```