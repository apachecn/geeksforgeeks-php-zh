# PHP|juliantojd()函数

> Original: [https://www.geeksforgeeks.org/php-juliantojd-function/](https://www.geeksforgeeks.org/php-juliantojd-function/)

Juliantojd()函数是 PHP 中的一个内置函数，用于将儒略历日期转换为儒略日计数。 儒略历的日期范围是从公元前 4713 年(基督之前)到公元 9999 年(阿诺·多米尼克)。

**语法：**

```php
int juliantojd( $month, $day, $year )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$Month：**必选参数，用于指定儒略历中的月份编号。 月份数字在 1(即 1 月)到 12(即 12 月)的范围内。
*   **$day：**必选参数，用于指定儒略历中的日期。 天数的范围在 1 到 31 之间。
*   **$Year：**必选参数，用于指定儒略历中的年份。 年份从-4713 到 9999。

**返回值：**此函数返回给定儒略日期的儒略日。
**例外：**儒略历的有效范围是公元前 4713 年到公元 9999 年。

下面的程序演示了 PHP 中的 juliantojd()函数。

**程序 1：**

## PHP

```php
<?php

// converts Julian calendar Date to
// Julian Day number.
$jdate = juliantojd(8, 30, 2018);

// printd the Julian Day Count
echo "Julian Day count: " . $jdate . "\n";

// converts Julian Day number to
// Julian calendar Date.
$julian = jdtojulian($jdate);

// prints the Julian calendar Date.
echo "Julian calendar: " . $julian;

?>
```

**Output**

```php
Julian Day count: 2458374
Julian calendar: 8/30/2018 

```

**程序 2：**

## PHP

```php
<?php

// convert Julian Calendar Date to Julian Day number.
$jdate = juliantojd(12, 3, 2001);

// prints the Julian calendar.
echo "Julian calendar " . $jdate . "\n";

// convert Julian calendar Date into julian Day number.
$julian = jdtojulian($jdate);

// print the Julian date number.
echo "Julian Date Count : " . $julian;
?>
```

**Output**

```php
Julian calendar 2452260
Julian Date Count : 12/3/2001 

```

**相关文章：**

*   [PHP|cal_day_in_Month()函数](https://www.geeksforgeeks.org/php-cal_days_in_month-function/)
*   [PHP|Easter_Days()函数](https://www.geeksforgeeks.org/php-easter_days-function/)

**引用：**[http://php.net/manual/en/function.juliantojd.php](http://php.net/manual/en/function.juliantojd.php)