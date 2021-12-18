# PHP|IntlCalendar Beer()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-before-function/](https://www.geeksforgeeks.org/php-intlcalendar-before-function/)

**IntlCalendar：：BEFORE()函数**是 PHP 中的一个内置函数，如果对象的当前时间早于传递的对象的当前时间，则返回 True。

**语法：**

*   Object-oriented style:

    ```php
    *bool* IntlCalendar::before( *IntlCalendar* $other )
    ```

*   Process style:

    ```php
    *bool* intlcal_before( *IntlCalendar* $cal, *IntlCalendar* $other )
    ```

**参数：**

*   **$cal:** this parameter saves IntlCalendar resources.
*   **$Other:** this parameter saves a calendar whose time is checked against the time of the main object.

**返回值：**如果对象的当前时间早于传递的对象的当前时间，则此函数返回 TRUE。

下面的程序演示了 PHP 中的 IntlCalendar：：Being()函数：

**程序：**

```php
<?php

// Create an IntlCalendar from a DateTime object or string
$calendar1 = IntlCalendar::fromDateTime('2019-08-29 09:19:29');

// Clone the Calendar date
$calendar2 = clone $calendar1;

// Use IntlCalendar::before() function
// and display result
var_dump($calendar1->before($calendar2));
var_dump($calendar2->before($calendar1));

// Use IntlCalendar::add() function to
// add month in date
$calendar1->add(IntlCalendar::FIELD_MONTH, 1);

// Use IntlCalendar::before() function
// and display result
var_dump($calendar1->before($calendar2));
var_dump($calendar2->before($calendar1));

?>
```

**输出：**

```php
bool(false)
bool(false)
bool(false)
bool(true)

```

**引用：**[https://www.php.net/manual/en/intlcalendar.before.php](https://www.php.net/manual/en/intlcalendar.before.php)