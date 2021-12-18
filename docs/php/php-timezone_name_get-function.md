# PHP|timezone_name_get()函数

> Original: [https://www.geeksforgeeks.org/php-timezone_name_get-function/](https://www.geeksforgeeks.org/php-timezone_name_get-function/)

TIMEZONE_NAME_GET()函数是 PHP 中的一个内置函数，用于返回时区的名称。 Date Time 对象作为参数发送给 timezone_name_get()函数，如果成功则返回时区名称，如果失败则返回 False。

**语法：**

```php
string timezone_name_get( $object )
```

**参数：**此函数接受单个参数*$Object*，这是必需的。 用于指定 DateTimeZone 对象。

**返回值：**此函数成功时返回时区名称，失败时返回 False。

**异常：**timezone_name_get()函数是 DateTimeZone：：getName()函数的别名。

下面的程序演示了 PHP 中的 timezone_name_get()函数：

**程序 1：**

```php
<?php

// Opening the timezone of America/Chicago
$timezone = timezone_open("America/Chicago");

// Displaying the name of the timezone
echo ("The name of the timezone is " . timezone_name_get($timezone));
?>
```

**输出：**

```php
The name of the timezone is America/Chicago

```

**程序 2：**

```php
<?php

// Opening the default timezone
echo ("Default time zone is " . date_default_timezone_get());
echo "\n";

// Declaring a new timezone
$new_timezone = 'America/Chicago';

if( date_default_timezone_set( $new_timezone) )
{
  echo "New time zone is ". date_default_timezone_get();
}

?>
```

**输出：**

```php
Default time zone is UTC
New time zone is America/Chicago

```

**相关文章：**

*   [php|TIMEZONE_LOCATION_GET()函数](https://www.geeksforgeeks.org/php-timezone_location_get-function/)
*   [PHP|TIMEZONE_NAME_FROM_ABBR()11-13](https://www.geeksforgeeks.org/php-timezone_name_from_abbr-function/)
*   [PHP|TIMEZONE_VERSION_GET()11-13](https://www.geeksforgeeks.org/php-timezone_version_get-function/)

**引用：**[http://php.net/manual/en/function.timezone-name-get.php](http://php.net/manual/en/function.timezone-name-get.php)