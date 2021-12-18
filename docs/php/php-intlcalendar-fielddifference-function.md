# PHP|IntlCalendar fieldDifference()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-fielddifference-function/](https://www.geeksforgeeks.org/php-intlcalendar-fielddifference-function/)

**IntlCalendar：：fieldDifference()函数**是 PHP 中的一个内置函数，用于返回给定时间和对象时间之间的差值。

**语法：**

*   Object-oriented style:

    ```php
    *int* IntlCalendar::fieldDifference( *float* $when, *int* $field )
    ```

*   Process style:

    ```php
    *int* intlcal_field_difference( *IntlCalendar* $cal, *float* $when, *int* $field )
    ```

**参数：**

*   **$cal:** this parameter saves the IntlCalendar resource name.
*   **$WHEN:** this parameter saves the time it takes to compare the quantity represented by the field.
*   **$field:** this parameter holds a field that represents the quantity to be compared.

**返回值：**此函数成功时返回与指定字段关联的单位的带符号时间差，失败时返回 False。

下面的程序演示了 PHP 中的 IntlCalendar：：fieldDifference()函数：

**程序：**

```php
<?php

// Set the timezone
ini_set('date.timezone', 'Asia/Calcutta');

// Get the time from calendar
$calendar1 = IntlCalendar::fromDateTime('2018-12-21 09:30:25');
$calendar2 = IntlCalendar::fromDateTime('2019-08-29 11:20:20');

// Get time represented by the object
$calTime = $calendar2->getTime();

// Display the first time
echo "First Time: " . IntlDateFormatter::formatObject($calendar1) . "\n";

// Display the last time
echo "Last Time: " . IntlDateFormatter::formatObject($calendar2) . "\n";

// Time difference
echo "Time difference: "
    . $calendar1->fieldDifference($calTime, 
            IntlCalendar::FIELD_YEAR) . "-Years "

    . $calendar1->fieldDifference($calTime,
            IntlCalendar::FIELD_MONTH) . "-Months "

    . $calendar1->fieldDifference($calTime, 
            IntlCalendar::FIELD_DAY_OF_MONTH) . "-Days "

    . $calendar1->fieldDifference($calTime, 
            IntlCalendar::FIELD_HOUR_OF_DAY) . "-Hours "

    . $calendar1->fieldDifference($calTime, 
            IntlCalendar::FIELD_MINUTE) . "-Minutes";

?>
```

**输出：**

```php
First Time: Dec 21, 2018, 9:30:25 AM
Last Time: Aug 29, 2019, 11:20:20 AM
Time difference: 0-Years 8-Months 8-Days 1-Hours 49-Minutes

```

**引用：**[https://www.php.net/manual/en/intlcalendar.fielddifference.php](https://www.php.net/manual/en/intlcalendar.fielddifference.php)