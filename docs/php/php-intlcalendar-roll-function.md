# PHP|IntlCalendar roll()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar-roll-function/](https://www.geeksforgeeks.org/php-intlcalendar-roll-function/)

**IntlCalendar：：roll()函数**是 PHP 中的一个内置函数，用于将值添加到字段中，而不会进入更重要的字段。 IntlCalendar：：Roll()函数和 IntlCalendar：：Add()函数的区别在于，IntlCalendar：：Roll()函数的字段值溢出，不会带入更重要的字段。
**语法：**和

*   面向对象的样式：

```php
*bool* IntlCalendar::roll( *int* $field, *mixed* $amountOrUpOrDown )
```

*   程序风格：

```php
*bool* intlcal_roll( *IntlCalendar* $cal, *int* $field, *mixed* $amountOrUpOrDown )
```

**参数：**μ

*   **$cal：**此参数保存 IntlCalendar 对象的资源。
*   **$field：**此参数保存 IntlCalendar 日期/时间字段常量之一。 字段常量的值是整数，介于 0 到 IntlCalendar：：Field_Count 之间。
*   **$accumtOrUpOrDown：**此参数保存要添加到字段中的已签名金额。 TRUE 值表示从 DATETIME 字段上滚(加 1)，FALSE 值表示下滚(减 1)。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。下面的程序说明了 PHP：
**程序：**和
中的 IntlCalendar：：Roll()函数

## PHP

```php
<?php

// Set the DateTime zone
ini_set('date.timezone', 'Asia/Calcutta');

// Create an instance of IntlCalendar
$calendar = IntlCalendar::createInstance('Asia/Calcutta');

// Set the DateTime to the calendar object
$calendar->set(2019, 8, 24);

// Display the calendar object
var_dump(IntlDateFormatter::formatObject($calendar));

// Roll down 1 day of date field
$calendar->roll(IntlCalendar::FIELD_DAY_OF_MONTH, false);

// Display the calendar object
var_dump(IntlDateFormatter::formatObject($calendar));

?>
```

**Output:** 

```php
string(24) "Sep 24, 2019, 8:29:48 AM"
string(24) "Sep 23, 2019, 8:29:48 AM"
```

**引用：**[https://www.php.net/manual/en/intlcalendar.roll.php](https://www.php.net/manual/en/intlcalendar.roll.php)