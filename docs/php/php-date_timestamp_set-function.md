# PHP|DATE_TIMESTAMP_SET()函数

> Original: [https://www.geeksforgeeks.org/php-date_timestamp_set-function/](https://www.geeksforgeeks.org/php-date_timestamp_set-function/)

DATE_TIMESTAMP_SET()函数是 PHP 中的一个内置函数，用于根据 Unix 时间戳设置日期和时间。 此函数用于方法链接时返回 DateTime 对象，失败时返回 False。

**语法：**

*   **process style:**

    ```php
    date_timestamp_set( $object, $unixtimestamp )
    ```

*   **object-oriented style:**

    ```php
    DateTime::setTimestamp( $unixtimestamp )
    ```

**参数：**此函数接受上述两个参数，如下所述：

*   **$object:** this is a mandatory parameter that specifies the DateTime object returned by the date_create () function.
*   **$unixtimeStamp:** this parameter is used to set the Unix timestamp that represents the date.

**返回值：**此函数成功时返回 DateTime 对象，失败时返回 False。

下面的程序演示了 PHP 中的 date_timeamp_set()函数：

**程序 1：**

```php
<?php

// Create DateTime object
$date = date_create();

// Display DateTime in given format
echo date_format($date, 'U = d-m-Y H:i:s') . "\n";

// date_timestamp_set function to Set
// Unix timestamp
date_timestamp_set($date, 1373502124);

// Display DateTime in given format
echo date_format($date, 'U = d-m-Y H:i:s');
?>
```

**输出：**

```php
1537159667 = 17-09-2018 04:47:47
1373502124 = 11-07-2013 00:22:04

```

**程序 2：**

```php
<?php

// Create DateTime object
$date = new DateTime();

// Display DateTime in given format
echo $date->format('U = d-m-Y H:i:s') . "\n";

// date_timestamp_set function to Set
// Unix timestamp
$date->setTimestamp(1171564674);

// Display DateTime in given format
echo $date->format('U = d-m-Y H:i:s');
?>
```

**输出：**

```php
1537159667 = 17-09-2018 04:47:47
1171564674 = 15-02-2007 18:37:54

```

**相关文章：**

*   __T0__PHP|DATE_DEFAULT_TIMEZONE_SET()_T1_
*   [php|DATE_GET_LAST_ERROR()函数](https://www.geeksforgeeks.org/php-date_get_last_errors-function/)
*   __T0__PHP|DATE_DEFAULT_TIMEZONE_GET()_T1_

**引用：**[http://php.net/manual/en/datetime.settimestamp.php](http://php.net/manual/en/datetime.settimestamp.php)