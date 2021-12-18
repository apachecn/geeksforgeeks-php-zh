# PHP|IntlCalendar After()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-after-function/](https://www.geeksforgeeks.org/php-intlcalendar-after-function/)

**IntlCalendar：：After()函数**是 PHP 中的一个内置函数，如果对象时间晚于传递对象的时间，则返回 True。

**语法：**

*   Object-oriented style:

    ```
    *bool* IntlCalendar::after( *IntlCalendar* $other )
    ```

*   Process style:

    ```
    *bool* intlcal_after( *IntlCalendar* $cal, *IntlCalendar* $other )
    ```

**参数：**

*   **$cal:** this parameter saves IntlCalendar resources.
*   **$Other:** this parameter saves the calendar, and the time of the calendar is checked against the time of the primary object.

**返回值：**如果对象时间晚于传递对象的时间，则此函数返回 True，否则返回 False。

下面的程序演示了 PHP 中的 IntlCalendar：：After()函数：

**程序：**

```
<?php

// Create an IntlCalendar from a DateTime object or string
$calendar1 = IntlCalendar::fromDateTime('2019-08-29 09:19:29');

// Clone the Calendar date
$calendar2 = clone $calendar1;

// Use IntlCalendar::after() function
// and display result
var_dump($calendar1->after($calendar2));
var_dump($calendar2->after($calendar1));

// Use IntlCalendar::add() function to
// add month in date
$calendar1->add(IntlCalendar::FIELD_MONTH, 1);

// Use IntlCalendar::after() function
// and display result
var_dump($calendar1->after($calendar2));
var_dump($calendar2->after($calendar1));

?>
```

**输出：**

```
bool(false)
bool(false)
bool(true)
bool(false)

```

**引用：**[https://www.php.net/manual/en/intlcalendar.after.php](https://www.php.net/manual/en/intlcalendar.after.php)