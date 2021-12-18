# PHP|IntlCalendar getFirstDayOfWeek()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-getfirstdayofweek-function/](https://www.geeksforgeeks.org/php-intlcalendar-getfirstdayofweek-function/)

**IntlCalendar：：getFirstDayOfWeek()函数**是 PHP 中的一个内置函数，用于返回日历的一周的第一天。

**语法：**

*   Object-oriented style

    ```
    *int* IntlCalendar::getFirstDayOfWeek( *void* )
    ```

*   Process style

    ```
    *int* intlcal_get_first_day_of_week( *IntlCalendar* $cal )
    ```

**参数：**此函数使用单个参数**$cal**，该参数保存 IntlCalendar 的资源。

**返回值：**此函数返回 IntlCalendar 字段常量之一，如 IntlCalendar：：Dow_SUNDAY，IntlCalendar：：Dow_Monday，…。 ，IntlCalendar：：Dow_Satday 表示成功，失败表示 FALSE。

下面的程序演示了 PHP 中的 IntlCalendar：：getFirstDayOfWeek()函数：

**程序：**

```
<?php

// Set the DateTime zone
ini_set('date.timezone', 'Asia/Calcutta');
ini_set('date.timezone', 'UTC');

// Set the DateTime object
$calendar1 = IntlCalendar::fromDateTime('2019-09-22');

// Use getFirstDayOfWeek() function to get
// the first day of week
var_dump($calendar1->getFirstDayOfWeek());

// Get the week of year
var_dump($calendar1->get(IntlCalendar::FIELD_WEEK_OF_YEAR));

// Create an instance of calendar
$calendar2 = IntlCalendar::createInstance(NULL, 'en_US');

// Use getFirstDayOfWeek() function to get
// the first day of week
var_dump($calendar2->getFirstDayOfWeek());

// Set the date to the calendar
$calendar2->set(2020, 05, 20);

// Check the given month is leap or not
var_dump($calendar2->get(IntlCalendar::FIELD_IS_LEAP_MONTH)); 

?>
```

**输出：**

```
int(1)
int(39)
int(1)
int(0)

```

**引用：**[https://www.php.net/manual/en/intlcalendar.getfirstdayofweek.php](https://www.php.net/manual/en/intlcalendar.getfirstdayofweek.php)