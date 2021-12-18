# PHP|date_offset_get()函数

> Original: [https://www.geeksforgeeks.org/php-date_offset_get-function/](https://www.geeksforgeeks.org/php-date_offset_get-function/)

DATE_OFFSET_GET()函数是 PHP 中的一个内置函数，用于返回时区偏移量。 此函数用于在成功时返回 UTC(协调世界时)的时区偏移量(以秒为单位)，如果失败则返回 False。

**语法：**

*   **process style:**

    ```
    int date_offset_get( $object )
    ```

*   **object-oriented style:**

    ```
    int DateTime::getOffset( void )
    int DateTimeImmutable::getOffset( void )
    int DateTimeInterface::getOffset( void )
    ```

**参数：**此函数接受单个参数*$Object*，这在过程样式中是必需的。 Date_create()函数返回的 DateTime 对象。 但在面向对象样式的情况下，不需要参数。

**返回值：**此函数成功时返回 UTC(协调世界时)的时区偏移量(以秒为单位)，失败时返回 False。

下面的程序演示了 PHP 中的 date_offset_get()函数：

**程序 1：**

```
<?php
$date1 = date_create('2018-09-12', timezone_open('Asia/Kolkata'));
$date2 = date_create('20018-09-18', timezone_open('Asia/Singapore'));

echo date_offset_get($date1) . "\n";
echo date_offset_get($date2) . "\n";
?>
```

**输出：**

```
19800
28800

```

**程序 2：**

```
<?php
$date1 = new DateTime('2018-09-12', new DateTimeZone('Asia/Kolkata'));
$date2 = new DateTimeImmutable('2018-09-18', new DateTimeZone('Asia/Singapore'));

echo $date1->getOffset() . "\n";
echo $date2->getOffset() . "\n";
?>
```

**输出：**

```
19800
28800

```

**相关文章：**

*   [PHP|date_date_set()11-13](https://www.geeksforgeeks.org/php-date_date_set-function/)
*   [php|DATE_PARSE_FROM_FORMAT()函数](https://www.geeksforgeeks.org/php-date_parse_from_format-function/)
*   [php|MicroTime()函数](https://www.geeksforgeeks.org/php-microtime-function/)

**引用：**[http://php.net/manual/en/datetime.getoffset.php](http://php.net/manual/en/datetime.getoffset.php)