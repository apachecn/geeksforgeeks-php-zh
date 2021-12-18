# PHP|IntlCalendar add()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-add-function/](https://www.geeksforgeeks.org/php-intlcalendar-add-function/)

**IntlCalendar：：add()函数**是 PHP 中的一个内置函数，用于将带符号的时间量添加到字段中。

**语法：**

*   面向对象的样式：

```php
*bool* IntlCalendar::add( *int* $field, *int* $amount ) 
```

*   程序风格：

```php
*bool* intlcal_add( *IntlCalendar* $cal, *int* $field, *int* $amount )
```

**参数：**

*   **$cal：**此参数保存 IntlCalendar 资源。
*   **$field：**此参数保存 IntlCalendar 日期/时间字段常量。 它保存介于 0 到 IntlCalendar：：field_count 之间的整数值。
*   **$Amount：**要添加到当前字段的已签名金额。 如果数量的值是正的，那么它将向前移动，如果数量的值是负的，那么它将移动到过去。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。下面的程序说明了 PHP：
**程序 1：**中的 IntlCalendar：：Add()函数

## PHP

```php
<?php

// Create an IntlCalendar from a DateTime object or string
$calendar = IntlCalendar::fromDateTime('2019-08-29 09:19:29');

// Add the date
$calendar->add(IntlCalendar::FIELD_MONTH, 1);

// Display the result date
echo IntlDateFormatter::formatObject($calendar), "\n";

// Add the date
$calendar->add(IntlCalendar::FIELD_WEEK_OF_MONTH, 1);

// Display the result output
echo IntlDateFormatter::formatObject($calendar);

?>
```

**Output:** 

```php
Sep 29, 2019, 9:19:29 AM
Oct 6, 2019, 9:19:29 AM
```