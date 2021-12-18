# PHP|IntlCalendar getTime()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-gettime-function/](https://www.geeksforgeeks.org/php-intlcalendar-gettime-function/)

**IntlCalendar：：getTime()函数**是 PHP 中的一个内置函数，用于返回对象当前表示的时间。 时间以自纪元以来的毫秒为单位表示。

**语法：**

*   Object-oriented style

    ```
    *float* IntlCalendar::getTime( *void* )
    ```

*   Process style

    ```
    *float* intlcal_get_time( *IntlCalendar* $cal )
    ```

**参数：**此函数接受单个参数**$cal**，该参数保存 IntlCalendar 对象的资源。

**返回值：**此函数返回一个浮点数，表示自纪元(1970 年 1 月 1 日 00：00：00 UTC)以来经过的毫秒数。

下面的程序演示了 PHP 中的 IntlCalendar：：getTime()函数：

**程序：**

```
<?php

// Create an instance of calendar
$calendar = IntlCalendar::createInstance();

// Get the current time
var_dump($calendar->getTime());

// Create a new IntlGregorianCalendar
$calendar = new IntlGregorianCalendar(2019, 9, 22, 12, 30, 56);

// Get the current time
var_dump($calendar->getTime());

// Create a DateTime object
$calendar = IntlCalendar::fromDateTime('2019-03-21 09:19:29');

// Get the current time
var_dump($calendar->getTime());

// Set the timezone
$calendar->setTimeZone('GMT+05:30');

// Get the current time
var_dump($calendar->getTime());

?>
```

**输出：**

```
float(1569306894500)
float(1571747456000)
float(1553159969000)
float(1553159969000)

```

**引用：**[https://www.php.net/manual/en/intlcalendar.gettime.php](https://www.php.net/manual/en/intlcalendar.gettime.php)