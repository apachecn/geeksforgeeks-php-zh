# PHP|IntlCalendar getLeastMaximum()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-getleastmaximum-function/](https://www.geeksforgeeks.org/php-intlcalendar-getleastmaximum-function/)

**IntlCalendar：：getLeastMaximum()函数**是 PHP 中的一个内置函数，用于获取字段的最小局部最大值。 该值应小于或等于 IntlCalendar：：getActualMaxmimum()，后者小于或等于 IntlCalendar：：getMaximum()返回值。

**语法：**

*   Object-oriented style

    ```
    *int* IntlCalendar::getLeastMaximum( *int* $field )
    ```

*   Process style

    ```
    *int* intlcal_get_least_maximum( *IntlCalendar* $cal, *int* $field )
    ```

**参数：**此函数使用上述两个参数：

*   **$cal:** this parameter saves the resources of IntlCalendar.
*   **$FIELD:** this parameter holds one of the IntlCalendar date / time field constants. The value of the field constant is an integer between 0 and IntlCalendar::Field_Count.

**返回值：**此函数返回整数值，成功时返回字段单位中的字段值，失败时返回 False。

下面的程序演示了 PHP 中的 IntlCalendar：：getLeastMaximum()函数：

**程序：**

```
<?php

// Set the date timezone
ini_set('date.timezone', 'Asia/Calcutta');
ini_set('intl.default_locale', 'en_US');

// Create a DateTime object
$calendar = IntlCalendar::fromDateTime('2019-03-21 09:19:29');

var_dump(
    $calendar->getLeastMaximum(IntlCalendar::FIELD_DAY_OF_MONTH),
    $calendar->getActualMaximum(IntlCalendar::FIELD_DAY_OF_MONTH),
    $calendar->getMaximum(IntlCalendar::FIELD_DAY_OF_MONTH), 
    $calendar->getLeastMaximum(IntlCalendar::FIELD_WEEK_OF_YEAR),
    $calendar->getActualMaximum(IntlCalendar::FIELD_WEEK_OF_YEAR),
    $calendar->getMaximum(IntlCalendar::FIELD_WEEK_OF_YEAR)
);
?>
```

**输出：**

```
int(28)
int(31)
int(31)
int(52)
int(52)
int(53)

```

**引用：**[https://www.php.net/manual/en/intlcalendar.getleastmaximum.php](https://www.php.net/manual/en/intlcalendar.getleastmaximum.php)