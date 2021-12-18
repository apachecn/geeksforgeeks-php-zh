# PHP | cal_to_jd()函数

> 原文:[https://www.geeksforgeeks.org/php-cal_to_jd-function/](https://www.geeksforgeeks.org/php-cal_to_jd-function/)

函数是 PHP 中的一个内置函数，用于将指定的日期转换为儒略日计数。 *cal_to_jd()* 函数计算指定日历中某个日期的儒略日计数。该功能支持 CAL_GREGORIAN、CAL_JULIAN、CAL _ JULIAN 和 CAL _ FRENCH 日历。
**语法:**

```
int cal_to_jd( $calendar, $month, $day, $year )
```

**参数:**该功能接受四个参数，如上所述，描述如下:

*   **$日历**:用于指定计算的日历。日历值有公历、法国历、犹太历和儒略历。
*   **$month** :用于指定所选日历中的月份。
*   **$day** :用于指定所选日历中的日期。
*   **$year** :用于指定所选日历中的年份。

**返回值:**该函数返回儒略日数字。
下面的程序说明了 PHP 中的 cal_to_jd()函数。
**节目 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Converts a Gregorian calendar Date
// into Julian Day number.
$date = cal_to_jd(CAL_GREGORIAN, 11, 03, 2007);

// Prints the conversion of date to
// Julain Day number.
echo $date;
?>
```

**Output:** 

```
2454408
```

**程序 2:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Converts Julian calendar Date into
// Julian Day count.
$date = cal_to_jd(CAL_JULIAN, 7, 20, 20017);

// Prints the above conversion.
echo $date;
?>
```

**Output:** 

```
9032468
```

**相关文章:**

*   [PHP | cal_days_in_month()函数](https://www.geeksforgeeks.org/php-cal_days_in_month-function/)
*   [PHP |复活节 _days()函数](https://www.geeksforgeeks.org/php-easter_days-function/)

**参考:**T2】http://php.net/manual/en/function.cal-to-jd.php