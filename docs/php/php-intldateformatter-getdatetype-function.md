# PHP|IntlDateForMatter getDateType()函数

> Original: [https://www.geeksforgeeks.org/php-intldateformatter-getdatetype-function/](https://www.geeksforgeeks.org/php-intldateformatter-getdatetype-function/)

**IntlDateForMatter：：getDateType()函数**是 PHP 中的一个内置函数，用于获取 IntlDateForMatter 对象使用的数据类型。

**语法：**

*   Object-oriented style:

    ```php
    *int* IntlDateFormatter::getDateType( *void* )
    ```

*   Process style:

    ```php
    *int* datefmt_get_datetype( *IntlDateFormatter* $fmt )
    ```

**参数：**此函数使用单个参数**$fmt**，该参数保存格式化程序的资源。

**返回值：**此函数返回格式化程序的当前日期类型值。

下面的程序演示了 PHP 中的 IntlDateForMatter：：getDateType()函数：

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

// Get the date/type formatter type
echo 'Calendar of formatter: '
        . datefmt_get_datetype($formatter) . "\n";

// Get the format of date/time value as a string
echo "Formatted calendar output: "
        . datefmt_format( $formatter , 0) . "\n\n";

// Create a date formatter
$formatter = datefmt_create(
    'en_US',
    IntlDateFormatter::SHORT,
    IntlDateFormatter::SHORT,
    'Asia/Kolkata',
    IntlDateFormatter::TRADITIONAL
);

// Get the date/type formatter type
echo 'Calendar of formatter: '
        . datefmt_get_datetype($formatter) . "\n";

// Get the format of date/time value as a string
echo "Formatted calendar output: "
        . datefmt_format( $formatter , 0);

?>
```

**输出：**

```php
Calendar of formatter: 0
Formatted calendar output: 01/01/1970

Calendar of formatter: 3
Formatted calendar output: 1/1/70, 5:30 AM

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

// Get the date/type formatter type
echo 'Calendar of formatter: '
        . $formatter->getDateType() . "\n";

// Get the format of date/time
// value as a string
echo "Formatted calendar output: "
        . $formatter->format(0) . "\n\n";

// Create a date formatter
$formatter = datefmt_create(
    'en_US',
    IntlDateFormatter::SHORT,
    IntlDateFormatter::SHORT,
    'Asia/Kolkata',
    IntlDateFormatter::TRADITIONAL
);

// Get the date/type formatter type
echo 'Calendar of formatter: '
        . $formatter->getDateType() . "\n";

// Get the format of date/time
// value as a string
echo "Formatted calendar output: "
        . $formatter->format(0);

?>
```

**输出：**

```php
Calendar of formatter: 0
Formatted calendar output: 01/01/1970

Calendar of formatter: 3
Formatted calendar output: 1/1/70, 5:30 AM

```

**引用：**[https://www.php.net/manual/en/intldateformatter.getdatetype.php](https://www.php.net/manual/en/intldateformatter.getdatetype.php)