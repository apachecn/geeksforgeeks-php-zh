# PHP|IntlCalendar getTimeZone()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-gettimezone-function/](https://www.geeksforgeeks.org/php-intlcalendar-gettimezone-function/)

**IntlCalendar：：getTimeZone()函数**是 PHP 中的一个内置函数，用于返回与此日历关联的时区对象。

**语法：**

*   Object-oriented style

    ```php
    *IntlTimeZone* IntlCalendar::getTimeZone( *void* )
    ```

*   Process style

    ```php
    *IntlTimeZone* intlcal_get_time_zone( *IntlCalendar* $cal )
    ```

**参数：**此函数接受单个参数**$cal**，该参数保存 IntlCalendar 对象的资源。

**返回值：**此函数返回与此日历关联的 IntlTimeZone 对象。

下面的程序演示了 PHP 中的 IntlCalendar：：getTimeZone()函数：

**程序：**

```php
<?php

// Set the date timezone
ini_set('date.timezone', 'Asia/Calcutta');
ini_set('intl.default_locale', 'en_US');

// Create an instance of calendar
$calendar = IntlCalendar::createInstance();

// Get the object of timezone 
print_r($calendar->getTimeZone());

// Create new IntlGregorianCalendar object
$calendar->setTimezone(new DateTimeZone('Asia/Singapore')); 

// Get the object of timezone 
print_r($calendar->getTimeZone());

// Set the timezone
$calendar->setTimeZone('GMT+05:30');

// Get the object of timezone 
print_r($calendar->getTimeZone());

// Set the timezone
$calendar->setTimeZone(IntlTimeZone::getGMT());

// Get the object of timezone 
print_r($calendar->getTimeZone());

?>
```

**输出：**

```php
IntlTimeZone Object
(
    [valid] => 1
    [id] => Asia/Calcutta
    [rawOffset] => 19800000
    [currentOffset] => 19800000
)
IntlTimeZone Object
(
    [valid] => 1
    [id] => Asia/Singapore
    [rawOffset] => 28800000
    [currentOffset] => 28800000
)
IntlTimeZone Object
(
    [valid] => 1
    [id] => GMT+05:30
    [rawOffset] => 19800000
    [currentOffset] => 19800000
)
IntlTimeZone Object
(
    [valid] => 1
    [id] => GMT
    [rawOffset] => 0
    [currentOffset] => 0
)

```

**引用：**[https://www.php.net/manual/en/intlcalendar.gettimezone.php](https://www.php.net/manual/en/intlcalendar.gettimezone.php)