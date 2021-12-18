# PHP|date_isodate_set()函数

> Original: [https://www.geeksforgeeks.org/php-date_isodate_set-function/](https://www.geeksforgeeks.org/php-date_isodate_set-function/)

DATE_ISODATE_SET()函数是 PHP 中的一个内置函数，用于设置 ISO(国际标准化组织)日期。 此函数根据 ISO 8601 标准设置日期，使用周和日偏移量而不是特定日期。

**语法：**

*   **process style:**

    ```php
    date_isodate_set ( $object, $year, $week, $day )
    ```

*   **object-oriented style:**

    ```php
    DateTime::setISODate ( $year, $week, $day )
    ```

**参数：**此函数接受上述四个参数，如下所述：

*   **$object:** this parameter is only used in the process style. This parameter is created by the date_create () function. This function modifies this object.
*   **$Year:** this parameter is used to set the year of the date.
*   **$Week:** this parameter sets the week of the date.
*   **$day:** this parameter sets the offset from the first day of the week.

**返回值：**此函数成功时返回方法链接的 DateTime 对象，失败时返回 False。

下面的程序演示了 PHP 中的 date_isodate_set()函数：

**程序 1：**

```php
<?php
$date = date_create();

date_isodate_set($date, 2018, 9);
echo date_format($date, 'Y-m-d') . "\n";

date_isodate_set($date, 2018, 8, 17);
echo date_format($date, 'Y-m-d') . "\n";

date_isodate_set($date, 2018, 12, 23);
echo date_format($date, 'Y-m-d') . "\n";

date_isodate_set($date, 2015, 8, 24);
echo date_format($date, 'Y-m-d');
?>
```

**输出：**

```php
2018-02-26
2018-03-07
2018-04-10
2015-03-11

```

**程序 2：**

```php
<?php
$date = new DateTime();

$date->setISODate(12, 05, 2018);
echo $date->format('d-m-Y') . "\n";

$date->setISODate(2018, 2, 27);
echo $date->format('Y-m-d') . "\n";
?>
```

**输出：**

```php
08-08-0017
2018-02-03

```

**相关文章：**

*   [php|Date_Parse()函数](https://www.geeksforgeeks.org/php-date_parse-function/)
*   [PHP|date_sunset()11-13](https://www.geeksforgeeks.org/php-date_sunset-function/)
*   [php|DATE_SUN_INFO()函数](https://www.geeksforgeeks.org/php-date_sun_info-function/)

**引用：**[http://php.net/manual/en/datetime.setisodate.php](http://php.net/manual/en/datetime.setisodate.php)