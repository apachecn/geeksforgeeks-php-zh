# PHP|timezone_location_get()函数

> Original: [https://www.geeksforgeeks.org/php-timezone_location_get-function/](https://www.geeksforgeeks.org/php-timezone_location_get-function/)

TIMEZONE_LOCATION_GET()函数是 PHP 中的一个内置函数，用于返回给定时区的位置信息。 Date Time 对象作为参数发送给 timezone_location_get()函数，成功时返回与时区相关的位置信息，失败时返回 False。

**语法：**

```
timezone_location_get( $object )
```

**参数：**此函数接受单个参数*$Object*，这是必需的。 用于指定 DateTimeZone 对象。

**返回值：**此函数成功时返回给定时区的位置信息，失败时返回 False。

**异常：**timezone_location_get()函数是 DateTimeZone：：getLocation()函数的别名。

下面的程序演示了 PHP 中的 timezone_location_get()函数：

**程序 1：**

```
<?php

// Opening a timezone
$timeZone = timezone_open("Asia/Kolkata");

// Displaying the location details of a timezone
echo "Location Details of the Specified Timezone: \n";

print_r(timezone_location_get($timeZone));
?>
```

**输出：**

```
Location Details of the Specified Timezone: 
Array
(
    [country_code] => IN
    [latitude] => 22.53333
    [longitude] => 88.36666
    [comments] => 
)

```

**程序 2：**

```
<?php

// Declaring a timezone
$timeZone = new DateTimeZone("Asia/Kolkata");

// Displaying the location details of a timezone
echo ("Location Details of the Specified Timezone:\n");

print_r($timeZone->getLocation());
?>
```

**输出：**

```
Location Details of the Specified Timezone:
Array
(
    [country_code] => IN
    [latitude] => 22.53333
    [longitude] => 88.36666
    [comments] => 
)

```

**相关文章：**

*   [PHP|TIMEZONE_OPEN()11-13](https://www.geeksforgeeks.org/php-timezone_open-function/)
*   [PHP|TIMEZONE_VERSION_GET()11-13](https://www.geeksforgeeks.org/php-timezone_version_get-function/)

**引用：**[http://php.net/manual/en/function.timezone-location-get.php](http://php.net/manual/en/function.timezone-location-get.php)