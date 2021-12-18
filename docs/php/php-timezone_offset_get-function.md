# PHP|TIMEZONE_OFFSET_GET()函数

> Original: [https://www.geeksforgeeks.org/php-timezone_offset_get-function/](https://www.geeksforgeeks.org/php-timezone_offset_get-function/)

TIMEZONE_OFFSET_GET()函数是 PHP 中的一个内置函数，用于从 GMT 返回时区偏移量。 Date-Time 对象和 Date-Time 作为参数发送给 timezone_Offset_get()函数，如果成功则返回以秒为单位的时区偏移量，如果失败则返回 False。

**语法：**

```php
int timezone_offset_get( $object, $datetime )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$object:** it is a required parameter for the specified DateTimeZone object.
*   **$DATETIME:** it is also a mandatory parameter that specifies the date / time at which the offset must be calculated.

**返回值：**成功时返回时区偏移量，失败时返回 False。

**异常：**timezone_offset_get()函数是 DateTimeZone：：getOffset()函数的别名。

下面的程序演示了 PHP 中的 timezone_offset_get()函数：

**程序 1：**

```php
<?php

// Open the timezone of America/Chicago
$timezone = timezone_open("America/Chicago");

// Displaying the offset of America/Chicago and Europe/Amsterdam
$datetime_eur = date_create("now", timezone_open("Europe/Amsterdam"));
echo timezone_offset_get($timezone, $datetime_eur);
?>
```

**输出：**

```php
-18000

```

**程序 2：**

```php
<?php

// Open the timezone of America/Chicago and Europe/Amsterdam
$timezone_chicago = new DateTimeZone("America/Chicago");
$timezone_amsterdam = new DateTimeZone("Europe/Amsterdam");

$chicago = new DateTime("now", $timezone_chicago);
$amsterdam = new DateTime("now", $timezone_amsterdam);

// Calculating the offset between the timezones   
$Offset = $timezone_amsterdam -> getOffset($chicago);

// Dumping the offset variable
var_dump($Offset);
?>
```

**输出：**

```php
int(7200)

```

**相关文章：**

*   [php|TIMEZONE_LOCATION_GET()函数](https://www.geeksforgeeks.org/php-timezone_location_get-function/)
*   __T0__PHP|TIMEZONE_OPEN()_
*   __T0__PHP|TIMEZONE_NAME_FROM_abbr()_

**引用：**[http://php.net/manual/en/function.timezone-offset-get.php](http://php.net/manual/en/function.timezone-offset-get.php)