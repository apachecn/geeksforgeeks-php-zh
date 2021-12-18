# PHP|IntlCalendar：：__Construct()函数

> Original: [https://www.geeksforgeeks.org/php-intlcalendar__construct-function/](https://www.geeksforgeeks.org/php-intlcalendar__construct-function/)

**IntlCalendar：：__Construct()函数**是 PHP 中的一个内置函数，用于创建用于禁止实例化的私有构造函数。

**语法：**

```
*private* IntlCalendar::__construct( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的 IntlCalendar：：__Construct()函数：

**程序：**

```
<?php

// Create an IntlCalendar from a DateTime object or string
$calendar = IntlCalendar::fromDateTime('2019-08-29 09:19:29');

// Add the date
$calendar->add(IntlCalendar::FIELD_YEAR, 5);

// Display the result date
echo IntlDateFormatter::formatObject($calendar), "\n";

// Add the date
$calendar->add(IntlCalendar::FIELD_YEAR, 10);

// Display the result output
echo IntlDateFormatter::formatObject($calendar), "\n";

// Add the date
$calendar->add(IntlCalendar::FIELD_HOUR_OF_DAY, 10);

// Display the result output
echo IntlDateFormatter::formatObject($calendar);

?>
```

**输出：**

```
Aug 29, 2024, 9:19:29 AM
Aug 29, 2034, 9:19:29 AM
Aug 29, 2034, 7:19:29 PM

```

**引用：**[https://www.php.net/manual/en/intlcalendar.construct.php](https://www.php.net/manual/en/intlcalendar.construct.php)