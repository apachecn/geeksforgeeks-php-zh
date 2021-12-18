# PHP|timezone_version_get()函数

> Original: [https://www.geeksforgeeks.org/php-timezone_version_get-function/](https://www.geeksforgeeks.org/php-timezone_version_get-function/)

TIMEZONE_VERSION_GET()函数是 PHP 中的一个内置函数，用于返回时区数据库的版本。 不需要在 timezone_version_get()函数中传递任何参数。

**语法：**

```php
string timezone_version_get()
```

**参数：**timezone_version_get()函数不需要任何参数。

**返回值：**它以字符串形式返回时区数据库的版本。

**异常**timezone_version_get()函数生成输出 0.system，因为 PHP 版本尚未升级。

下面的程序演示了 PHP 中的 timezone_version_get()函数：

**程序：**

```php
<?php

// Displaying the version of the timezone database
$timezone_db= timezone_version_get();

echo ("Timezone Database Version: " . $timezone_db );
?>
```

**输出：**

```php
Timezone Database Version: 0.system

```

**引用：**[http://php.net/manual/en/function.timezone-version-get.php](http://php.net/manual/en/function.timezone-version-get.php)