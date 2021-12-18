# PHP 中如何将数字转换成月份名称？

> 原文:[https://www . geesforgeks . org/如何将数字转换为月份名称 php/](https://www.geeksforgeeks.org/how-to-convert-number-to-month-name-in-php/)

月号可以用 PHP 函数转换成月份名。有两个函数可以将给定的月号转换成月名。

**方法 1:使用 [mktime()函数](https://www.geeksforgeeks.org/php-mktime-function/):**mktime()函数是 PHP 中的一个内置函数，用于返回日期的 Unix 时间戳。时间戳返回一个长整数，包含 Unix Epoch(1970 年 1 月 1 日，格林尼治时间 00:00:00)和指定时间之间的秒数。小时、分钟、秒、月、日和年作为参数发送给 mktime()函数，成功时返回整数 Unix 时间戳，出错时返回 False。

**语法:**

```
int mktime( $hour, $minute, $second, $month, $day, $year, $is_dst)
```

**例:**

```
<?php
// PHP program to convert number to month name

// Declare month number and initialize it
$month_num =12;

// Use mktime() and date() function to
// convert number to month name
$month_name = date("F", mktime(0, 0, 0, $month_num, 10));

// Display month name
echo $month_name."\n";

?>
```

**输出:**

```
December

```