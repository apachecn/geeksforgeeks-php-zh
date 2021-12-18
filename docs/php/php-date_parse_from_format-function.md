# PHP|date_parse_from_format()函数

> Original: [https://www.geeksforgeeks.org/php-date_parse_from_format-function/](https://www.geeksforgeeks.org/php-date_parse_from_format-function/)

DATE_PARSE_FROM_FORMAT()是 PHP 中的一个内置函数，用于获取根据指定格式格式化的给定日期的信息。 函数的作用是：接受两个参数，并返回包含给定日期详细信息的关联数组。

**语法：**

```php
array date_parse_from_format ( $format, $date )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$format:** is used to specify the required parameters for the date format. The following parameter strings are used in the format.
    1.  **date:**
        *   **d and j:** indicate the day of the month, 2 digits, with or without leading zeros.
        *   The literal representation of **d and l:** for one day.
        *   **S:** the English serial number suffix of the month date, 2 characters. It is ignored in processing.
        *   **z:** date of the year (starting at 0)
    2.  **month:**
        *   **F and M:** the text representation of the month, such as January or September
        *   The number of **m and n:** months, with or without leading zeros
    3.  **year:**
        *   **Y:** full digital representation of the year, 4 digits
        *   **Y: two-digit representation of** year (assuming in the range 1970-2069, including)
    4.  **time:**
        *   **an and A: before and after** meridian
        *   **g and h:** 12-hour format with or without leading zeros
        *   **G and H:** 24-hour format with or without leading zeros
        *   **G and H:** 24-hour format. ]
        *   **I:** minutes, leading zero
        *   **s:** seconds with leading zero
        *   **u:** microseconds (up to 6 bits)
    5.  **time zone:**
        *   Time zone identifiers, or the hour difference with UTC, or the colon difference between hours and minutes and UTC, or the time zone abbreviation
    6.  **full date / time:**
        *   **U:** from the Unix era (00:00:00 GMT on January 1st, 1970)
    7.  **spaces and delimiters:**
        *   **(space): Tab**
        *   **#:** one of the following delimiters:;,:, /,., -, (Or)
        *   **;,:, /,., -, (Or): the character specified by** .
        *   **? :** random bytes
        *   ***:** random bytes up to the next delimiter or number
        *   **! :** resets all fields (year, month, day, hour, minute, second, score, and time zone information) to the Unix era
        *   **|:** reset all fields to the Unix era
        *   **|:** . Convert score and time zone information to Unix era (if they have not already been parsed)
        *   **+:** if this format specifier exists, the trailing data in the string will not cause an error, but will issue a warning
*   **$Date:** this is a mandatory parameter used to represent a date.

**返回值：**此函数返回包含日期详细描述的数组。

下面的程序演示了 PHP 中的 date_parse_from_format()函数。

```php
<?php

// Declare and initialize date variable.
$date = "0.9.2018 5:00+01:00";

// Function is used to return the detail about date.
print_r(date_parse_from_format("j.n.Y H:iP", $date));
?>
```

**Output:**

```php
Array
(
    [year] => 2018
    [month] => 9
    [day] => 0
    [hour] => 5
    [minute] => 0
    [second] => 0
    [fraction] => 
    [warning_count] => 1
    [warnings] => Array
        (
            [19] => The parsed date was invalid
        )

    [error_count] => 0
    [errors] => Array
        (
        )

    [is_localtime] => 1
    [zone_type] => 1
    [zone] => -60
    [is_dst] => 
)

```

**程序 2：**

```php
<?php

// Declare and initialize date variable.
$date = "2015.0.9";

// Function is used to return the detail about date.
print_r(date_parse_from_format("Y.z.n", $date));
?>
```

**输出：**

```php
Array
(
    [year] => 2015
    [month] => 9
    [day] => 1
    [hour] => 
    [minute] => 
    [second] => 
    [fraction] => 
    [warning_count] => 0
    [warnings] => Array
        (
        )

    [error_count] => 0
    [errors] => Array
        (
        )

    [is_localtime] => 
)

```

**相关文章：**

*   [php|DATE_SUN_INFO()函数](https://www.geeksforgeeks.org/php-date_sun_info-function/)
*   [PHP|date_sunset()11-13](https://www.geeksforgeeks.org/php-date_sunset-function/)
*   [php|Date_Parse()函数](https://www.geeksforgeeks.org/php-date_parse-function/)

**引用：**[http://php.net/manual/en/function.date-parse-from-format.php](http://php.net/manual/en/function.date-parse-from-format.php)