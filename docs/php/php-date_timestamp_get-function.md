# PHP|date_timeamp_get()函数

> Original: [https://www.geeksforgeeks.org/php-date_timestamp_get-function/](https://www.geeksforgeeks.org/php-date_timestamp_get-function/)

DATE_TIMESTAMP_GET()函数是 PHP 中的一个内置函数，用于获取 Unix 时间戳。 此函数返回代表日期的 Unix 时间戳。

**语法：**

*   **process style:**

    ```
    int date_timestamp_get( $object )
    ```

*   **object-oriented style:**

    ```
    int DateTime::getTimestamp( void )
    int DateTimeImmutable::getTimestamp( void )
    int DateTimeInterface::getTimestamp( void )
    ```

**参数：**此函数接受单个参数*$Object*，这是必需的。 它用于指定 date_create()函数返回的 DateTime 对象。 它仅在程序样式中使用。 面向对象样式不接受任何参数。

**返回值：**此函数返回代表日期的 Unix 时间戳。

下面的程序演示了 PHP 中的 date_timeamp_get()函数：

**程序 1：**

```
<?php

// Create DateTime object
$date = date_create();

// Display Unix timestamp date
echo date_timestamp_get($date);
?>
```

**输出：**

```
1537162804

```

**程序 2：**

```
<?php

// Create DateTime object
$date = new DateTime();

// Display Unix timestamp date
echo $date->getTimestamp();
?>
```

**输出：**

```
1537162805

```

**相关文章：**

*   [PHP|date_date_set()11-13](https://www.geeksforgeeks.org/php-date_date_set-function/)
*   [php|DATE_OFFSET_GET()函数](https://www.geeksforgeeks.org/php-date_offset_get-function/)
*   [php|gmstrftime()函数](https://www.geeksforgeeks.org/php-gmstrftime-function/)

**引用：**[http://php.net/manual/en/datetime.gettimestamp.php](http://php.net/manual/en/datetime.gettimestamp.php)