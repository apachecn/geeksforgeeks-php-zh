# PHP|IntlCalendar getActualMinimum()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-getactualminimum-function/](https://www.geeksforgeeks.org/php-intlcalendar-getactualminimum-function/)

**IntlCalendar：：getActualMinimum()函数**是 PHP 中的一个内置函数，用于返回当前时间附近的字段相对最小值。

**语法：**

*   Object-oriented style

    ```
    *int* IntlCalendar::getActualMinimum( *int* $field )
    ```

*   Process style

    ```
    *int* intlcal_get_actual_minimum( *IntlCalendar* $cal, *int* $field )
    ```

**参数：**此函数使用上述两个参数：

*   **$cal:** this parameter saves the resources of IntlCalendar.
*   **$FIELD:** this parameter holds one of the IntlCalendar date / time field constants. This field contains an integer value between 0 and IntlCalendar::Field_Count.

**返回值：**此函数返回整数值，该整数值表示与给定字段关联的单位中的最小值(如果成功)或 False(如果失败)。

下面的程序演示了 PHP 中的 IntlCalendar：：getActualMinimum()函数：

**程序：**

```
<?php

// Set the DateTime object
ini_set('date.timezone', 'Asia/Calcutta');

// Declare an IntlCalendar DateTime object
$calendar = IntlCalendar::fromDateTime('2010-09-22');

// Use getActualMaximum() function to the DateTime object
var_dump($calendar->getActualMinimum(IntlCalendar::FIELD_DAY_OF_MONTH));

// Use getActualMaximum() function to the DateTime object
var_dump($calendar->getActualMinimum(IntlCalendar::FIELD_DAY_OF_WEEK_IN_MONTH));

var_dump($calendar->getActualMinimum(IntlCalendar::FIELD_MONTH));

var_dump($calendar->getActualMinimum(IntlCalendar::FIELD_WEEK_OF_YEAR));

var_dump($calendar->getActualMinimum(IntlCalendar::FIELD_WEEK_OF_MONTH));

?>
```

**输出：**

```
int(1)
int(-1)
int(0)
int(1)
int(1)

```

**引用：**[https://www.php.net/manual/en/intlcalendar.getactualminimum.php](https://www.php.net/manual/en/intlcalendar.getactualminimum.php)