# PHP|IntlCalendar setTime()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-settime-function/](https://www.geeksforgeeks.org/php-intlcalendar-settime-function/)

**IntlCalendar：：setTime()函数**是 PHP 中的一个内置函数，用于设置日历时间对象，单位为从纪元开始的毫秒。 日历时间瞬间由浮点数表示，其值应为自纪元(1970 年 1 月 1 日 00：00：00.000 UTC)以来的整数毫秒数。 它忽略了闰秒。

**语法：**

*   Object-oriented style

    ```
    *bool* IntlCalendar::setTime( *float* $date )
    ```

*   Process style

    ```
    *bool* intlcal_set_time( *IntlCalendar* $cal, *float* $date )
    ```

**参数：**此函数使用上述两个参数：

*   **$cal:** this parameter saves the resources of IntlCalendar.
*   **$DATE:** this parameter saves the moment represented by the number of milliseconds between the moment and the Epoch time. It ignores leap seconds.

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的程序演示了 PHP 中的 IntlCalendar：：setTime()函数：

**程序：**

```
<?php

// Set the date timezone
ini_set('date.timezone', 'Asia/Calcutta');

// Create a DateTime object
$cal = IntlCalendar::fromDateTime('2019-03-21 09:19:29');

// Format the DateTime object 
echo IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL), "\n";

// Declare a new IntlGregorianCalendar object
$cal = new IntlGregorianCalendar(2019, 8, 22, 10, 30, 34);

// Format the DateTime object 
echo IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL), "\n";

// Set the DateTime object
$cal->setTime(strtotime('2019-10-27 -05:30:00 GMT') * 1000);

// Format the DateTime object 
echo IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL);

?>
```

**输出：**

```
Thursday, March 21, 2019 at 9:19:29 AM India Standard Time
Sunday, September 22, 2019 at 10:30:34 AM India Standard Time
Thursday, January 1, 1970 at 5:30:00 AM India Standard Time

```

**引用：**[https://www.php.net/manual/en/intlcalendar.settime.php](https://www.php.net/manual/en/intlcalendar.settime.php)