# PHP|IntlCalendar isEquivalentTo()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-isequivalentto-function/](https://www.geeksforgeeks.org/php-intlcalendar-isequivalentto-function/)

**IntlCalendar：：isEquivalentTo()函数**是 PHP 中的一个内置函数，用于检查给定的日历是否相等，但时间不同。

**语法：**

*   Object-oriented style

    ```
    *bool* IntlCalendar::isEquivalentTo( *IntlCalendar* $other )
    ```

*   Process style

    ```
    *bool* intlcal_is_equivalent_to( *IntlCalendar* $cal, *IntlCalendar* $other )
    ```

**参数：**此函数使用两个参数，如上所述，如下所述：

*   **$cal:** this parameter holds the resources of the IntlCalendar object.
*   **$Other:** this parameter saves another calendar to perform the comparison.

**返回值：**如果日历相同(可能只是设置的时间不同)，则此函数返回 TRUE，如果未设置参数值，则返回错误。

下面的程序演示了 PHP 中的 IntlCalendar：：isEquivalentTo()函数：

**程序：**

```
<?php

// Set the DateTime zone
ini_set('date.timezone', 'Asia/Calcutta');

// Create an instance of IntlCalendar
$calendar1 = IntlCalendar::createInstance('Asia/Calcutta');

// Create an instance of another IntlCalendar
$calendar2 = IntlCalendar::createInstance();

// Check whether another calendar is equal
// but for a different time
var_dump($calendar1->isEquivalentTo($calendar2));

// Create a DateTime object
$calendar1 = IntlCalendar::fromDateTime('2019-09-24');

// Set the date to another DateTime object
$calendar2->set(2019, 8, 24);

// Check whether another calendar is equal
// but for a different time
var_dump($calendar1->isEquivalentTo($calendar2));

?>
```

**输出：**

```
bool(true)
bool(true)

```

**引用：**[https://www.php.net/manual/en/intlcalendar.isequivalentto.php](https://www.php.net/manual/en/intlcalendar.isequivalentto.php)