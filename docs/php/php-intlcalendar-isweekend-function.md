# PHP|IntlCalendar isWeekend()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-isweekend-function/](https://www.geeksforgeeks.org/php-intlcalendar-isweekend-function/)

**IntlCalendar：：isWeekend()函数**是 PHP 中的一个内置函数，用于检查给定的日期/时间是否在周末。

**语法：**

*   Object-oriented style

    ```php
    *bool* IntlCalendar::isWeekend( *float* $date = NULL )
    ```

*   Process style

    ```php
    *bool* intlcal_is_weekend( *IntlCalendar* $cal, *float* $date = NULL )
    ```

**参数：**此函数使用两个参数，如上所述，如下所述：

*   **$cal:** this parameter holds the resources of the IntlCalendar object.
*   **$DATE:** this parameter holds an optional timestamp that represents the number of milliseconds since the era (excluding leap seconds). If the value of this parameter is empty, the current time is used.

**返回值：**此函数返回表示给定时间是否发生在周末的布尔值。

下面的程序演示了 PHP 中的 IntlCalendar：：isWeekend()函数：

**程序：**

```php
<?php

// Set the DateTime zone
ini_set('date.timezone', 'Asia/Calcutta');

// Create an instance of IntlCalendar
$calendar = IntlCalendar::createInstance('Asia/Calcutta');

// Check the given DateTime is weekend or not
var_dump($calendar->isWeekend());

// Set the DateTime to the object
$calendar->set(2019, 8, 29);

// Check the given DateTime is weekend or not
var_dump($calendar->isWeekend());

// Set the DateTime object
$calendar->isWeekend(strtotime('2019-09-22 12:30:00'));

// Check the given DateTime is weekend or not
var_dump($calendar->isWeekend());

?>
```

**输出：**

```php
bool(false)
bool(true)
bool(true)

```

**引用：**[https://www.php.net/manual/en/intlcalendar.isweekend.php](https://www.php.net/manual/en/intlcalendar.isweekend.php)