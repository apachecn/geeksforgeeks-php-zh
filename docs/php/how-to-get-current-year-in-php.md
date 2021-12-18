# PHP 中如何获取当前年份？

> 原文:[https://www . geesforgeks . org/如何获取当前年份 php/](https://www.geeksforgeeks.org/how-to-get-current-year-in-php/)

日期是一个用于格式化时间戳的内置函数。计算机在 UNIX 时间戳中存储日期和时间。这个时间是以 1970 年 1 月 1 日以来的秒数来计算的。由于这对于人类来说是不切实际的，PHP 将时间戳转换为人类可读且更容易理解的格式。

**语法:**

```
date( format, timestamp )
```

**说明:**

*   The format parameter in the date () function specifies the format of the returned date and time.
*   Timestamp is an optional parameter. If not, the current date and time will be used.

为了将当前年份作为四位数，Y 被用作参数 to date()函数，如下图所示:

**程序:**

```
<?php 
// PHP program to get the
// current year

echo "Current Year is :"; 

// Store the year to
// the variable
$year = date("Y"); 

// Display the year
echo $year; 

?> 
```

**Output:**

```
Current Year is :2019

```

**date()函数中可用的格式选项:**date()函数的格式参数是一个可以包含多个字符的字符串，允许以各种格式生成日期，如下所示:

*   D- indicates the day of the week (Monday to Sunday) in the text.
*   M–The leading zero (01 or 12) indicates the month.
*   M- indicates the month in the text, abbreviated as (January to December).
*   Y–use two digits (08 or 14) to represent the year.
*   Y–use four digits to represent the year (2008 or 2014).

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。