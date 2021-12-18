# PHP|IntlCalendar isset()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-isset-function/](https://www.geeksforgeeks.org/php-intlcalendar-isset-function/)

**IntlCalendar：：isset()函数**是 PHP 中的一个内置函数，用于检查给定字段是否已设置。 此函数与 IntlCalendar：：Clear()函数相反。

**语法：**

*   Object-oriented style

    ```php
    *bool* IntlCalendar::isSet( *int* $field )
    ```

*   Process style

    ```php
    *bool* intlcal_is_set( *IntlCalendar* $cal, *int* $field )
    ```

**参数：**此函数使用两个参数，如上所述，如下所述：

*   **$cal:** this parameter holds the resources of the IntlCalendar object.
*   **$FIELD:** this parameter holds one of the IntlCalendar date / time field constants. The value of the field constant is an integer between 0 and IntlCalendar::Field_Count.

**返回值：**如果设置了字段，则此函数返回 TRUE，如果未设置，则返回 ERROR。

下面的程序演示了 PHP 中的 IntlCalendar：：isset()函数：

**程序：**

```php
<?php

// Set the DateTime zone
ini_set('date.timezone', 'Asia/Calcutta');

// Create an instance of IntlCalendar
$calendar = IntlCalendar::createInstance('Asia/Calcutta');

// Check month field is set or not
var_dump($calendar->isSet(IntlCalendar::FIELD_MONTH));

// Set the DateTime to the object
$calendar->set(2019, 8, 29);

// Check for month field
var_dump($calendar->isSet(IntlCalendar::FIELD_MONTH));

// Set the DateTime object
$calendar->set(strtotime('2019-09-22 12:30:00'));

// Check for year field
var_dump($calendar->isSet(IntlCalendar::FIELD_YEAR));

?>
```

**输出：**

```php
bool(true)
bool(true)
bool(true)

```

**引用：**[https://www.php.net/manual/en/intlcalendar.isset.php](https://www.php.net/manual/en/intlcalendar.isset.php)