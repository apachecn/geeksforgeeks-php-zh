# PHP | checkdate()函数

> 原文:[https://www.geeksforgeeks.org/php-checkdate-function/](https://www.geeksforgeeks.org/php-checkdate-function/)

**checkdate()** 函数是 PHP 中的内置函数，用于检查参数中传递的日期的有效性。它接受格式为**毫米/日/年**年的日期。该函数返回一个布尔值。如果日期有效，则返回 true，否则返回 false。

**语法:**

```php
checkdate ( $month, $day, $year )
```

**参数:**该功能接受三个强制参数，如上所示，如下所述:

1.  **$ month**–该参数指定月份。有效日期的月份必须在 1 到 12 之间。
2.  **$ day**–该参数指定日期。日期可以在 1-31 的范围内，具体取决于输入的有效日期月份。如果是闰年，日期在 1-29 范围内，对于非闰年，日期在 1-28 范围内。
3.  **$ year**–该参数指定年份。年份必须在 1-32767(包括 1-32767)的范围内，具体取决于美元月和美元日，才能成为有效日期。

**返回值:**函数返回一个布尔值。如果传递的日期是有效日期，则返回 true。如果传递的日期无效，则返回 false。
**例:**

```php
Input : $month = 12 $day = 31 $year = 2017
Output : true

Input : $month = 2 $day = 29 $year = 2016
Output : true 

Input : $month = 2 $day = 29 $year = 2017
Output : false
```

下面的程序说明了 PHP 中的 checkdate()函数:
**程序 1:** 下面的程序检查日期是否有效。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
// PHP program to demonstrate the checkdate() function

$month = 12;
$day = 31;
$year = 2017;

// returns a boolean value after validation of date
var_dump(checkdate($month, $day, $year));

?>
```

**输出:**

```php
bool(true)
```

**程序 2:** 在闰年和非闰年的情况下，下面的程序检查日期是否有效。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
// PHP program to demonstrate the checkdate() function
// in case of leap year

$month = 2;
$day = 29;
$year = 2016;

// returns a boolean value after validation of date
// leap year
var_dump(checkdate($month, $day, $year));

$month = 2;
$day = 29;
$year = 2017;

// returns a boolean value after validation of date
// non-leap year
var_dump(checkdate($month, $day, $year));

?>
```

**输出:**

```php
bool(true)
bool(false)
```

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。