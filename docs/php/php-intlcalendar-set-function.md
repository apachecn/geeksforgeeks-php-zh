# PHP|IntlCalendar set()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-set-function/](https://www.geeksforgeeks.org/php-intlcalendar-set-function/)

**IntlCalendar：：Set()函数**是 PHP 中的一个内置函数，用于一次设置时间字段或几个公共字段。 字段值的范围取决于日历。 如果只有四个参数，则不能调用此函数。

**语法：**

*   面向对象样式

    ```php
    *bool* IntlCalendar::set( *int* $field, *int* $value )
    ```

    或

    ```php
    *bool* IntlCalendar::set( *int* $year, *int* $month, *int* $dayOfMonth = NULL,
                   *int* $hour = NULL, *int* $minute = NULL, *int* $second = NULL )
    ```

*   过程化样式

    ```php
    *bool* intlcal_set( *IntlCalendar* $cal, *int* $field, *int* $value )
    ```

    或

    ```php
    *bool* intlcal_set( *IntlCalendar* $cal, *int* $year, *int* $month, *int* $dayOfMonth = NULL,
                  *int* $hour = NULL, *int* $minute = NULL, *int* $second = NULL )
    ```

**参数：**此函数接受上述许多参数，如下所述：

*   **$cal：**此参数保存 IntlCalendar 对象的资源。
*   **$field：**此参数保存 IntlCalendar 日期/时间字段常量之一。 字段常量是介于 0 到 IntlCalendar：：Field_Count 之间的整数值。
*   **$value：**此参数保存给定字段的新值。
*   **$Year：**此参数保存 IntlCalendar：：Field_Year 字段的新值。
*   **$Month：**此参数保存 IntlCalendar：：Field_Month 字段的新值。
*   **$DayOfMonth：**此参数保存 IntlCalendar：：field_day_of_Month 字段的新值。 月份的顺序从零开始，即 0 表示 1 月，1 表示 2 月，依此类推。
*   **$Hour：**此参数保存 IntlCalendar：：field_hr_of_day 字段的新值。
*   **$Minint：**此参数保存 IntlCalendar：：Field_Minint 字段的新值。
*   **$Second：**此参数保存 IntlCalendar：：Field_Second 字段的新值。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的程序演示了 PHP 中的 IntlCalendar：：Set()函数：

**程序：**

```php
<?php

// Set the DateTime zone
ini_set('date.timezone', 'Asia/Calcutta');
ini_set('date.timezone', 'UTC');

// Create an instance of IntlCalendar
$calendar = IntlCalendar::createInstance('Asia/Calcutta');

// Set the DateTime object
$calendar->set(2019, 8, 24);

// Display the calendar object
var_dump(IntlDateFormatter::formatObject($calendar));

// Declare a new IntlGregorianCalendar object
$calendar = new IntlGregorianCalendar(2016, 8, 24);

// Set the year field
$calendar->set(IntlCalendar::FIELD_YEAR, 2018);

// Display the calendar object
var_dump(IntlDateFormatter::formatObject($calendar));

?>
```

**输出：**

```php
string(24) "Sep 24, 2019, 8:23:53 AM"
string(25) "Sep 24, 2018, 12:00:00 AM"

```

**引用：**[https://www.php.net/manual/en/intlcalendar.set.php](https://www.php.net/manual/en/intlcalendar.set.php)