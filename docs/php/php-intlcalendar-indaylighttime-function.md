# PHP|IntlCalendar inDaylightTime()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-indaylighttime-function/](https://www.geeksforgeeks.org/php-intlcalendar-indaylighttime-function/)

**IntlCalendar：：inDaylightTime()函数**是 PHP 中的一个内置函数，用于检查对象时间是否采用夏令时。

**语法：**

*   Object-oriented style

    ```php
    *bool* public IntlCalendar::inDaylightTime( *void* )
    ```

*   Process style

    ```php
    *bool* intlcal_in_daylight_time( *IntlCalendar* $cal )
    ```

**参数：**此函数接受单个参数**$cal**，它保存 IntlCalendar 对象的资源。

**返回值：**如果日期为夏令时，则此函数返回 TRUE，否则返回 FALSE。

下面的程序演示了 PHP 中的 IntlCalendar：：inDaylightTime()函数：

**程序：**

```php
<?php

// Set the DateTime zone
ini_set('date.timezone', 'Europe/Lisbon');

// Create an instance of IntlCalendar
$calendar = IntlCalendar::createInstance('Europe/Lisbon');

// Check whether the object time is in
// Daylight Savings Time or not
var_dump($calendar->inDaylightTime());

// Set the month field of IntlCalendar
$calendar->set(IntlCalendar::FIELD_MONTH, 11);

// Check whether the object time is in
// Daylight Savings Time or not
var_dump($calendar->inDaylightTime());

// Declare a IntlGregorianCalendar object
$calendar = new IntlGregorianCalendar(2019, 8, 24, 12, 40, 10);

// Check whether the object time is in
// Daylight Savings Time or not
var_dump($calendar->inDaylightTime());

// Set the date to DateTime object
$calendar->set(2019, 8, 24);

// Check whether the object time is in
// Daylight Savings Time or not
var_dump($calendar->inDaylightTime());

?>
```

**输出：**

```php
bool(true)
bool(false)
bool(true)
bool(true)

```

**引用：**[https://www.php.net/manual/en/intlcalendar.indaylighttime.php](https://www.php.net/manual/en/intlcalendar.indaylighttime.php)