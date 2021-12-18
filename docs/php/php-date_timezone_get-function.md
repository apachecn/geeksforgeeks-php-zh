# PHP|date_timezone_get()函数

> Original: [https://www.geeksforgeeks.org/php-date_timezone_get-function/](https://www.geeksforgeeks.org/php-date_timezone_get-function/)

DATE_TIMEZONE_GET()函数是 PHP 中的一个内置函数，用于返回相对于给定日期时间的时区。 此函数成功时返回 DateTimeZone 对象，失败时返回 False。

**语法：**

*   **process style:**

    ```php
    date_timezone_get( $object )
    ```

*   **object-oriented style:**

    ```php
    DateTime::getTimezone( void )
    DateTimeImmutable::getTimezone( void )
    DateTimeInterface::getTimezone( void )
    ```

**参数：**此函数接受单个参数*$Object*，这在过程样式中是必需的。 它用于指定 date_create()函数返回的 DateTime 对象。 面向对象的样式不需要任何参数。

**返回值：**此函数成功时返回 DateTimeZone 对象，失败时返回 False。

下面的程序演示了 PHP 中的 date_timezone_get()函数：

**程序 1：**

```php
<?php

// Create DateTime object
$date = date_create(null, timezone_open('Asia/Kolkata'));

// Return the timezone of given DateTime
$time_zone = date_timezone_get($date);

// Return the DateTimeZone object
echo timezone_name_get($time_zone);
?>
```

**输出：**

```php
Asia/Kolkata

```

**程序 2：**

```php
<?php

// Create DateTime object using DateTimeZone
$date = new DateTime(null, new DateTimeZone('Asia/Kolkata'));

// Return the timezone of given DateTime
$time_zone = $date->getTimezone();

// Return the DateTimeZone object
echo $time_zone->getName();
?>
```

**输出：**

```php
Asia/Kolkata

```

**相关文章：**

*   __T0__PHP|TIMEZONE_VERSION_GET()_
*   [PHP|gmdate()11-13](https://www.geeksforgeeks.org/php-gmdate-function/)
*   [PHP|date_date_set()11-13](https://www.geeksforgeeks.org/php-date_date_set-function/)

**引用：**[http://php.net/manual/en/datetime.gettimezone.php](http://php.net/manual/en/datetime.gettimezone.php)