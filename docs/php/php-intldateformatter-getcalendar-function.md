# PHP|IntlDateForMatter getCalendar()函数

> Original: [https://www.geeksforgeeks.org/php-intldateformatter-getcalendar-function/](https://www.geeksforgeeks.org/php-intldateformatter-getcalendar-function/)

**IntlDateForMatter：：getCalendar()函数**是 PHP 中的一个内置函数，用于返回 IntlDateForMatter 对象使用的日历类型。

**语法：**

*   Object-oriented style:

    ```php
    *int* IntlDateFormatter::getCalendar( *void* )
    ```

*   Process style:

    ```php
    *int* datefmt_get_calendar( *IntlDateFormatter* $fmt )
    ```

**参数：**此函数接受保存格式化程序资源的单个参数**$fmt**。

**返回值：**此函数返回格式化程序使用的日历类型。 Formatter 对象可以是 IntlDateForMatter：：Tradition 或 IntlDateForMatter：：Gregorian。

下面的程序演示了 PHP 中的 IntlDateForMatter：：getCalendar()函数：

**程序 1：**

```php
<?php

// Create a date formatter
$formatter = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'Asia/Kolkata',
    IntlDateFormatter::TRADITIONAL,
    "MM/dd/yyyy"
);

// Get the calendar type
echo 'Calendar of formatter: ' 
        . datefmt_get_calendar($formatter) . "\n";

// Get the format of date/time value as a string
echo "Formatted calendar output: "
        . datefmt_format( $formatter , 0) . "\n\n";

// Set the calendar type used by the formatter
datefmt_set_calendar($formatter,
        IntlDateFormatter::GREGORIAN);

// Get the calendar type
echo 'Calendar of formatter: ' 
        . datefmt_get_calendar($formatter) . "\n";

// Get the format of date/time value as a string
echo "First Formatted output is "
        . datefmt_format( $formatter , 0);

?>
```

**输出：**

```php
Calendar of formatter: 0
Formatted calendar output: 01/01/1970

Calendar of formatter: 1
First Formatted output is 01/01/1970

```

**程序 2：**

```php
<?php

// Create a date formatter
$formatter = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'Asia/Kolkata',
    IntlDateFormatter::TRADITIONAL,
    "MM/dd/yyyy"
);

// Get the calendar type
echo 'Calendar of formatter: ' 
        . $formatter->getCalendar() . "\n";

// Get the format of date/time value as a string
echo "Formatted calendar output: "
        . $formatter->format(0) . "\n\n";

// Set the calendar type used by the formatter
$formatter->setCalendar(IntlDateFormatter::GREGORIAN);

// Get the calendar type
echo 'Calendar of formatter: ' 
        . $formatter->getCalendar() . "\n";

// Get the format of date/time value as a string
echo "First Formatted output is "
        . $formatter->format(0);

?>
```

**输出：**

```php
Calendar of formatter: 0
Formatted calendar output: 01/01/1970

Calendar of formatter: 1
First Formatted output is 01/01/1970

```

**引用：**[https://www.php.net/manual/en/intldateformatter.getcalendar.php](https://www.php.net/manual/en/intldateformatter.getcalendar.php)