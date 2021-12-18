# PHP|date_default_timezone_set()函数

> Original: [https://www.geeksforgeeks.org/php-date_default_timezone_set-function/](https://www.geeksforgeeks.org/php-date_default_timezone_set-function/)

DATE_DEFAULT_TIMEZONE_SET()函数是 PHP 中的一个内置函数，用于设置脚本中所有日期/时间函数使用的默认时区。 如果时区无效，则此函数返回 False，否则返回 True。

**语法：**

```php
bool date_default_timezone_set( $timezone_identifier )
```

**参数：**此函数接受单个参数*$timezone_IDENTIFIER*，这是必需的。 此参数设置时区标识符，如 UTC 或 Asia/Kolkata。

**返回值：**如果 TIMEZONE_IDENTIFIER 无效，则此函数返回 False，否则返回 True。

下面的程序演示了 PHP 中的 date_default_timezone_set()函数：

**程序 1：**

```php
<?php

// Set timezone
date_default_timezone_set('Asia/Kolkata');

// Create 
$timezone_object = date_default_timezone_get();

// Compare the timezone with ini-set timezone
if (strcmp($timezone_object, ini_get('date.timezone'))){
    echo 'Script timezone differs from ini-set timezone.';
} else {
    echo 'Script timezone and ini-set timezone match.';
}
?>
```

**输出：**

```php
Script timezone differs from ini-set timezone.

```

**程序 2：**

```php
<?php

// Set the timezone
date_default_timezone_set('Asia/Dubai');

// Create the timezone object
$timezone_object = date_default_timezone_get();

// Compare the timezone with ini-set timezone
if (strcmp($timezone_object, ini_get('date.timezone'))){
    echo 'Script timezone differs from ini-set timezone.';
} else {
    echo 'Script timezone and ini-set timezone match.';
}
?>
```

**输出：**

```php
Script timezone differs from ini-set timezone.

```

**相关文章：**

*   [php|Date_Parse()函数](https://www.geeksforgeeks.org/php-date_parse-function/)
*   [PHP|date_sunset()11-13](https://www.geeksforgeeks.org/php-date_sunset-function/)
*   [php|DATE_SUN_INFO()函数](https://www.geeksforgeeks.org/php-date_sun_info-function/)

**引用：**[http://php.net/manual/en/function.date-default-timezone-set.php](http://php.net/manual/en/function.date-default-timezone-set.php)