# PHP|date_timezone_set()函数

> Original: [https://www.geeksforgeeks.org/php-date_timezone_set-function/](https://www.geeksforgeeks.org/php-date_timezone_set-function/)

DATE_TIMEZONE_SET()函数是 PHP 中的一个内置函数，用于设置 DateTime 对象的时区。 此函数返回 DateTime 对象，如果失败则返回 False。

**语法：**

*   **process style:**

    ```
    date_timezone_set( $object, $timezone )
    ```

*   **object-oriented style:**

    ```
    DateTime::setTimezone( $timezone )
    ```

**参数：**此函数接受上述两个参数，如下所述：

*   **$object:** this is a mandatory parameter that specifies the DateTime object returned by the date_create () function.
*   **$TimeZone:** this parameter is used to set the DateTimeZone object that represents the desired time zone.

**返回值：**此函数成功时返回 DateTime 对象，失败时返回 False。

下面的程序演示了 PHP 中的 date_timezone_set()函数：

**程序 1：**

```
<?php

// Create DateTime object
$date = date_create('2018-09-15', timezone_open('Asia/Kolkata'));

// Display the date format
echo date_format($date, 'd-m-Y H:i:sP') . "\n";

// Set the date time zone
date_timezone_set($date, timezone_open('Asia/Singapore'));

// Display the date format
echo date_format($date, 'd-m-Y H:i:sP');
?>
```

**输出：**

```
15-09-2018 00:00:00+05:30
15-09-2018 02:30:00+08:00

```

**程序 2：**

```
<?php

// Create DateTime object
$date = new DateTime('2018-09-15', new DateTimeZone('Asia/Kolkata'));

// Display the date format
echo $date->format('d-m-Y H:i:sP') . "\n";

// Set the date time zone
$date->setTimezone(new DateTimeZone('Asia/Singapore'));

// Display the date format
echo $date->format('d-m-Y H:i:sP');
?>
```

**输出：**

```
15-09-2018 00:00:00+05:30
15-09-2018 02:30:00+08:00

```

**相关文章：**

*   [php|time_nanosept()函数](https://www.geeksforgeeks.org/php-time_nanosleep-function/)
*   __T0__PHP|TIMEZONE_NAME_FROM_abbr()_

**引用：**[http://php.net/manual/en/datetime.settimezone.php](http://php.net/manual/en/datetime.settimezone.php)