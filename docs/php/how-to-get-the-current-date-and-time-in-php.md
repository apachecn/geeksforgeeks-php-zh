# 如何在 PHP 中获取当前日期和时间？

> 原文:[https://www . geesforgeks . org/如何获取当前的 php 日期和时间/](https://www.geeksforgeeks.org/how-to-get-the-current-date-and-time-in-php/)

本文的目的是用 PHP 获取当前的日期和时间。使用简单的内置 PHP 函数[**【date()**](https://www.geeksforgeeks.org/php-date-time/)**执行。**日期是用于格式化*时间戳*的内置函数。计算机在 UNIX 时间戳中存储日期和时间。这个时间是以 1970 年 1 月 1 日以来的秒数来计算的。由于这对于人类来说很难阅读，PHP 将时间戳转换为人类可读且更容易理解的格式。

**语法:**

```php
date('d-m-y h:i:s');
```

**参数:****日期()**参数不同。每个参数代表一些有意义的单位。

1.  **d:** 表示一个月中有两位数字带前导零的日子(01 或 31)
2.  **m:** 用前导零(01 或 1)表示月份
3.  **y:** 用两位数(08 或 14)表示一年。
4.  **h:** 用两位数字表示一天中的小时，前导零(01 或 1)
5.  **I:** 表示当前时区的分钟。
6.  **s:** 表示当前时区的秒数。

**例 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php 
// PHP program to get the 
// current date and time 

echo "Current date and time is :"; 

// Store the date and time  to 
// the variable 
$myDate = date("d-m-y h:i:s");

// Display the date and time 
echo $myDate; 

?> 
```

**输出:**

```php
Current date and time is :03-01-21 04:49:52
```

**例 2:** 下面演示了其他 **date()** 函数格式，开发者可以根据需要使用。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<!DOCTYPE html>
<html>
<body>
<h2>Other ways of using date() function</h2>
<?php
echo "Date in Year.Month.Day format is: " 
    . date("Y.m.d") . "<br>";

echo "Date in Year-Month-day format is: " 
    . date("Y-m-d") . "<br>";

echo "Date in Year/Month/day format is: " 
    . date("Y/m/d") . "<br>";

?>
</body>
</html>
```

**输出:**

![](img/9c2aaa4eda9e53ce85e4bd375a4962e5.png)