# PHP | cal_from_jd()函数

> 原文:[https://www.geeksforgeeks.org/php-cal_from_jd-function/](https://www.geeksforgeeks.org/php-cal_from_jd-function/)

cal_from_jd()函数是 PHP 中的一个内置函数，用于将儒略日计数转换为受支持的日历，如公历、法国历、犹太历等。该函数接受两个参数 *$jd* 和 *$calendar* ，并返回包含指定日历的日历信息的数组。

**语法:**

```php
array cal_from_jd( $jd, $calendar )
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **$ JD:** Used to specify the Julian day as an integer.
*   **$ calendar:** The calendar used to specify the conversion date. The supported calendars are Gregorian calendar, julian calendar calendar, French calendar and Jewish calendar.

**返回值:**该函数返回一个包含日历信息的数组，列表如下:

*   The date is in the form of "month/day/year"
*   moon
*   year
*   What day is it
*   Abbreviations and full names of working days and months

**程序 1:**

```php
<?php

// PHP program to implement cal_from_jd()
// and convert date to the CAL_GREGORIAN 

$input = unixtojd(mktime(0, 0, 0, 8, 16, 2016));
print_r(cal_from_jd($input, CAL_GREGORIAN));
?> 
```

**Output:**

```php
Array
(
    [date] => 8/16/2016
    [month] => 8
    [day] => 16
    [year] => 2016
    [dow] => 2
    [abbrevdayname] => Tue
    [dayname] => Tuesday
    [abbrevmonth] => Aug
    [monthname] => August
)

```

**程序二:**

```php
<?php

// PHP program to implement cal_from_jd() 
// and convert date to the CAL_JEWISH calender
$today = unixtojd(mktime(0, 0, 0, 6, 20, 2007));

print_r(cal_from_jd($today, CAL_JEWISH));
?>
```

**输出:**

```php
Array
(
    [date] => 11/4/5767
    [month] => 11
    [day] => 4
    [year] => 5767
    [dow] => 3
    [abbrevdayname] => Wed
    [dayname] => Wednesday
    [abbrevmonth] => Tammuz
    [monthname] => Tammuz
)

```

**相关文章:**

*   [PHP | julianjd()98o](https://www.geeksforgeeks.org/php-juliantojd-function/)
*   [PHP | jdtojulian()98o](https://www.geeksforgeeks.org/php-jdtojulian-function/)

**参考:**T2】http://php.net/manual/en/function.cal-from-jd.php