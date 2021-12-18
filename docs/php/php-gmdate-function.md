# PHP|gmdate()函数

> Original: [https://www.geeksforgeeks.org/php-gmdate-function/](https://www.geeksforgeeks.org/php-gmdate-function/)

Gmdate()是 PHP 中的一个内置函数，用于格式化 GMT/UTC 日期和时间并返回格式化的日期字符串。 它类似于 date()函数，但它返回格林威治标准时间(GMT)的时间。

**语法：**

```
string gmdate ( $format, $timestamp )
```

**参数：**gmdate()函数接受如上所述的两个参数：

*   **$format:** this is a required parameter that specifies the format of the date and time to be returned.
*   **$TIMESTAMP:** TIMESTAMP is an optional parameter, if not included, the current date and time are used.

**返回值：**此函数成功时返回格式化的日期字符串，失败时返回 False，并返回 E_WARNING。

下面的程序演示了 gmdate()函数。

**程序 1：**

```
<?php
// PHP program to illustrate gmdate function

// display date Jun 25 2018 23:21:50
echo gmdate("M d Y H:i:s",
        mktime(23, 21, 50, 6, 25, 2018)) ."\n";

// display date  World Wide Web Consortium
// 2018-06-25T23:21:50+00:00
echo gmdate(DATE_W3C,
        mktime(23, 21, 50, 6, 25, 2018)). "\n";

// display date as ISO-8601 format
echo gmdate(DATE_ISO8601,
        mktime(23, 21, 50, 6, 25, 2018)). "\n";

?>
```

**输出：**

```
Jun 25 2018 23:21:50
2018-06-25T23:21:50+00:00
2018-06-25T23:21:50+0000

```

**程序 2：**传递一个参数，则返回当前本地时间(time())。

```
<?php
// PHP program to illustrate gmdate function

// display current date and time 
// Jun 28 2018 14:52:50
echo gmdate("M d Y H:i:s") ."\n";

// display date  World Wide Web Consortium
echo gmdate(DATE_W3C). "\n";

// display date as ISO-8601 format
echo gmdate(DATE_ISO8601). "\n";

?>
```

**输出：**

```
Jun 29 2018 06:32:34
2018-06-29T06:32:34+00:00
2018-06-29T06:32:34+0000

```

**相似文章：**

*   [PHP | date and time](https://www.geeksforgeeks.org/php-date-time/)
*   [PHP | time () function](https://www.geeksforgeeks.org/php-time-function/)

**引用：**[http://php.net/manual/en/function.gmdate.php](http://php.net/manual/en/function.gmdate.php)