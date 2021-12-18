# 如何在 PHP 中获取字符串长度？

> 原文:[https://www . geeksforgeeks . org/如何获取 php 中的字符串长度/](https://www.geeksforgeeks.org/how-to-get-string-length-in-php/)

在本文中，我们学习如何在 PHP 中找到字符串的长度。

**方法:**这个任务可以使用 PHP 中的内置函数 [**strlen()**](https://www.geeksforgeeks.org/php-strlen-function/) 来完成。此方法用于返回字符串的长度。它返回一个代表给定字符串长度的数值。

**语法:**

```php
strlen($string)
```

**例 1:**

## PHP

```php
<?php
// PHP program to count all
// characters in a string
$str = "GeeksforGeekslover";

// Using strlen() function to
// get the length of string
$len = strlen($str);

// Printing the result
echo $len;
?>
```

**输出:**

```php
18
```

**示例 2:** 下面的代码演示了在 PHP 中使用 **strlen()** 函数，其中字符串具有特殊字符和转义序列。

## PHP

```php
<?php
// PHP program to find the length of
// a given string which has special
// characters
$str = "\n LuckyGeeks ;";

// Here '\n' has been counted as 1
echo strlen($str);
?>
```

**输出:**

```php
14
```