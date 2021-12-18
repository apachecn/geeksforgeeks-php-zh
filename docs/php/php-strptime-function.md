# PHP|strptime()函数

> Original: [https://www.geeksforgeeks.org/php-strptime-function/](https://www.geeksforgeeks.org/php-strptime-function/)

Strptime()函数是 PHP 中的内置函数，用于解析由 strftime()函数生成的时间/日期。 日期和格式作为参数发送给 strptime()函数，成功时返回数组，失败时返回 False 数组。 Strptime()函数返回的数组包含以下参数：

*   **tm_sec:** it represents the number of seconds after a minute (0-61).
*   **tm_min:** indicates hours (0-59)
*   **tm_hr:** means from midnight (0-23)
*   **tm_mday:** indicates the day of the month (1-31)
*   **tm_ . Since January (0-11)**
*   **tm_Year:** represents the year since 1900
*   **tm_WDAY:** since Sunday (0-6)
*   **tm_yday:** since January 1st (0365)
*   The number of days since [. Indicates that the specified format is not used

识别的日期部分

**语法：**

```php
array strptime( $date, $format )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$date:** it is a mandatory parameter that specifies the string to parse.
*   **$FORMAT:** required parameter that specifies the format used in the date.

**返回值：**此函数成功时返回数组，失败时返回 False。

下面的程序演示了 PHP 中的 strptime()函数：

**程序 1：**

```php
<?php

// Declaring the format of date/time
$format = "%d/%m/%Y %H:%M:%S";

// Parsing the date/time
$dt = strftime( $format );
echo "$dt";
print_r(strptime( $dt, $format ));
?>
```

**输出：**

```php
22/08/2018 11:46:57Array
(
    [tm_sec] => 57
    [tm_min] => 46
    [tm_hour] => 11
    [tm_mday] => 22
    [tm_mon] => 7
    [tm_year] => 118
    [tm_wday] => 3
    [tm_yday] => 233
    [unparsed] => 
)

```

**程序 2：**

```php
<?php

// Ddeclaring a different format of date/time
$format="%d/%m/%y %I:%M:%S";

// Parsing the date/time
$dt = strftime( $format );
echo "$dt";
print_r(strptime( $dt, $format ));
?>
```

**输出：**

```php
22/08/18 11:46:59Array
(
    [tm_sec] => 59
    [tm_min] => 46
    [tm_hour] => 11
    [tm_mday] => 22
    [tm_mon] => 7
    [tm_year] => 118
    [tm_wday] => 3
    [tm_yday] => 233
    [unparsed] => 
)

```

**相关文章：**

*   [PHP|gmdate()11-13](https://www.geeksforgeeks.org/php-gmdate-function/)
*   [php|Date_Parse()函数](https://www.geeksforgeeks.org/php-date_parse-function/)

**引用：**[http://php.net/manual/en/function.strptime.php](http://php.net/manual/en/function.strptime.php)