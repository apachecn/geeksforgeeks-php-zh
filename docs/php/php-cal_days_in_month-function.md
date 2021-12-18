# PHP | cal_days_in_month()函数

> 原文:[https://www . geesforgeks . org/PHP-cal _ days _ in _ month-function/](https://www.geeksforgeeks.org/php-cal_days_in_month-function/)

PHP 中的 cal_days_in_month()函数是一个内置函数，用于根据特定的日历(如公历、法国日历、犹太日历等)返回特定年份一个月中的天数。

cal_days_in_month()函数接受三个参数，即日历、月和年，并根据指定的月、年和日历返回天数。

**语法:**

```
cal_days_in_month($calendar, $month, $year)
```

**参数:**PHP 中的 cal_days_in_month()函数接受三个参数，如下所述:

1.  **$calendar** :指定你要考虑的日历，比如法语、公历、犹太教等。
2.  **$month** :指定你选择的日历中的月份。
3.  **$year** :指定你选择的日历中的年份。

**返回值:**根据指定的月、年、日历返回天数。

**错误和异常**:

1.  当使用的日期在 1550 年之前时，cal_days-in_month 函数给出错误的输出。
2.  cal_days-in_month 函数给出了闰年发现之前的日期的错误输出。

**示例:**

```
Input: cal_days_in_month(CAL_JEWISH, 2, 1966);
Output: 29
Explanation: February 1966 had 29 days.

Input: cal_days_in_month(CAL_GREGORIAN, 2, 2004);
Output: 29
Explanation: February 2004 had 29 days

```

以下程序说明了 cal_days_in_month()函数:

**程序 1** :

```
<?php

// Using cal_days_in_month() function to
// know the number of days in february, 1966
$days = cal_days_in_month(CAL_JEWISH, 2, 1966);

echo "February 1966 had $days days.<br>";

?>
```

输出:

```
February 1966 had 29 days.
```

**程序 2** :

```
<?php

// Using cal_days_in_month() function to
// know the number of days in february, 2004
$days = cal_days_in_month(CAL_GREGORIAN, 2, 2004);

echo "February 2004 had $days days";

?>
```

输出:

```
February 2004 had 29 days
```

**参考:**T2[http://php.net/manual/en/function.cal-days-in-month.php](http://php.net/manual/en/function.cal-days-in-month.php)