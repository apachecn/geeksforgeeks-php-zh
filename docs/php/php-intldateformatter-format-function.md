# PHP|IntlDateForMatter Format()函数

> Original: [https://www.geeksforgeeks.org/php-intldateformatter-format-function/](https://www.geeksforgeeks.org/php-intldateformatter-format-function/)

**IntlDateForMatter：：Format()函数**是 PHP 中的一个内置函数，用于将日期/时间值格式化为字符串。

**语法：**

*   Object-oriented style:

    ```php
    *string* IntlDateFormatter::format( *mixed* $value )
    ```

*   Process style:

    ```php
    *string* datefmt_format( *IntlDateFormatter* $fmt, *mixed* $value )
    ```

**参数：**此函数使用上述两个参数：

*   **fmt:** this parameter saves the resources of the Date object.
*   **value:** this parameter saves the value in format. It can be a DateTimeInterface object, an IntlCalendar object, or a numeric type that represents the number of seconds. If a DateTime or IntlCalendar object is passed, it is not considered.

**返回值：**此函数成功时返回格式化字符串，出错时返回 False。

下面的程序演示了 PHP 中的 IntlDateForMatter：：Format()函数：

**程序：**

```php
<?php

// Create a date formatter
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::LONG,
    IntlDateFormatter::LONG,
    'Asia/Kolkata',
    IntlDateFormatter::GREGORIAN
);

// Display the date in given format
echo 'Formatted output using object oriented style: '
            . $fmt->format(0) . "\n";

echo 'Formatted output using procedural style: '
            . datefmt_format($fmt, 0) . "\n\n";

// Create a date formatter
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::SHORT,
    IntlDateFormatter::SHORT,
    'Asia/Kolkata',
    IntlDateFormatter::GREGORIAN
);

// Display the date in given format
echo 'Formatted output using object oriented style: '
            . $fmt->format(0) ."\n";

echo 'Formatted output using procedural style: '
            . datefmt_format($fmt, 0);

?>
```

**输出：**

```php
Formatted output using object oriented style: January 1, 1970 at 5:30:00 AM GMT+5:30
Formatted output using procedural style: January 1, 1970 at 5:30:00 AM GMT+5:30

Formatted output using object oriented style: 1/1/70, 5:30 AM
Formatted output using procedural style: 1/1/70, 5:30 AM

```

**引用：**[https://www.php.net/manual/en/intldateformatter.format.php](https://www.php.net/manual/en/intldateformatter.format.php)