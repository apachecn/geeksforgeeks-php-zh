# PHP|date_default_timezone_get()函数

> Original: [https://www.geeksforgeeks.org/php-date_default_timezone_get-function/](https://www.geeksforgeeks.org/php-date_default_timezone_get-function/)

DATE_DEFAULT_TIMEZONE_GET()函数是 PHP 中的一个内置函数，用于获取脚本中所有日期/时间函数使用的默认时区。

**语法：**

```php
string date_default_timezone_get( void )
```

**参数：**此函数不接受任何参数。
**返回值：**此函数返回字符串。

**注意：**此函数通过以下方式返回默认时区：

*   使用 date_default_timezone_set()函数读取时区。
*   在 PHP 5.4.0 之前，读取 TZ 环境变量。
*   读取 date.timezone ini 选项的值
*   PHP 5.4.0 之前，查询主机操作系统(如果操作系统支持并允许)。 这使用了一种必须猜测时区的算法。

如果上述任何语句不正确，则 date_default_timezone_get()将返回 UTC 的默认时区。下面的程序说明了 PHP 中的 date_default_timezone_get()函数：

**程序 1：**

## PHP

```php
<?php

// Set the default timezone
date_default_timezone_set('Asia/Kolkata');

// Create timezone object
$timezone_object = date_default_timezone_get();

// If timezone object is true
if ($timezone_object) {
    echo 'date_default_timezone_set: ' . date_default_timezone_get();
}
?>
```

**Output:** 

```php
date_default_timezone_set: Asia/Kolkata
```

**程序 2：**

## PHP

```php
<?php

// Set the default timezone
date_default_timezone_set('Asia/Kolkata');

echo date_default_timezone_get() . ' => ' . date('e') . ' => ' . date('T');
?>
```

**Output:** 

```php
Asia/Kolkata => Asia/Kolkata => IST
```

**相关文章：**

*   [PHP|date_sun_info()函数](https://www.geeksforgeeks.org/php-date_sun_info-function/)
*   [PHP|date_parse()函数](https://www.geeksforgeeks.org/php-date_parse-function/)
*   [PHP|date_sunset()函数](https://www.geeksforgeeks.org/php-date_sunset-function/)

**引用：**[http://php.net/manual/en/function.date-default-timezone-get.php](http://php.net/manual/en/function.date-default-timezone-get.php)