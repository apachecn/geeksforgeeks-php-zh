# PHP|TIMEZONE_OPEN()函数

> Original: [https://www.geeksforgeeks.org/php-timezone_open-function/](https://www.geeksforgeeks.org/php-timezone_open-function/)

Timezone_open()函数是 PHP 中的一个内置函数，用于创建新的 DateTimeZone 对象。 函数的作用是：接受时区作为参数，成功时返回 DateTimeZone 对象，失败时返回 False。

**语法：**

```
timezone_open( $timezone )
```

**参数：**此函数接受单个参数*$timezone*，这是必需的。 它指定要创建的新 DateTimeZone 对象的时区。

**返回值：**成功时返回 DateTimeZone 对象，失败时返回 False。

**异常：**作为参数传递的时区必须是 PHP 支持的时区，否则可能会导致错误的结果。

下面的程序演示了 PHP 中的 timezone_open()函数：

**程序 1：**

```
<?php

// Creating a new DateTimeZone object
$timezone = timezone_open("America/Chicago");

echo ("The new DateTimeZone object created is " 
              . timezone_name_get($timezone ));
?>
```

**Output:**

```
The new DateTimeZone object created is America/Chicago

```

**程序 2：**

```
<?php

// Array of timezones
$timezones = array('Europe/London', 'Asia/Kolkata');
foreach ($timezones as $tz) {
    $name = timezone_open($tz);

    echo ("The new DateTimeZone object created is "
                . timezone_name_get($name). "<br>");
}
?>
```

**Output:**

```
The new DateTimeZone object created is Europe/London
The new DateTimeZone object created is Asia/Kolkata

```

**注意：**TIMEZONE_OPEN()函数发出警告，因为传递的时区不是支持的/有效的时区。

**引用：**[http://php.net/manual/en/function.timezone-open.php](http://php.net/manual/en/function.timezone-open.php)