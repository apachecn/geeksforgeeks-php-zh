# 如何用 PHP 将大写字符串转换成小写？

> 原文:[https://www . geesforgeks . org/如何使用-php/](https://www.geeksforgeeks.org/how-to-convert-uppercase-string-to-lowercase-using-php/) 将大写字符串转换为小写字符串

在 PHP 中将大写字符串转换为小写的最好方法是使用[**strtolow()**](https://www.geeksforgeeks.org/php-strtolower-function/)**函数。它将字符串作为输入，将其所有字符转换为小写，并返回字符串值。**

****语法:****

```
string strtolower( $string )
```

****返回值:**返回转换为低位字符串的字符串。**

****例 1:****

## **PHP**

```
<?php
  echo strtolower("GeeksForGeeks")
?>
```

****输出:****

```
geeksforgeeks
```