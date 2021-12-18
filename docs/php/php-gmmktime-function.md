# PHP|gmmktime()函数

> Original: [https://www.geeksforgeeks.org/php-gmmktime-function/](https://www.geeksforgeeks.org/php-gmmktime-function/)

Gmmktime()函数是 PHP 中的一个内置函数，用于返回 GMT 日期的 Unix 时间戳。 *$小时、$分钟、$秒、$月、$日、$年*和*$IS_DST*作为参数发送到 gmmktime()函数，如果成功则返回整数 Unix 时间戳，如果出错则返回 FALSE。

**语法：**

```
int gmmktime( $hour, $minute, $second, $month, $day, $year, $is_dst)
```

**参数：**此函数接受上述 7 个参数，如下所述：

*   **$hr：**可选参数，用于指定小时时间。
*   **$分钟：**可选参数，用于指定分钟。
*   **$Second：**可选参数，用于指定第二个参数。
*   **$Month：**可选参数，用于指定月份。
*   **$day：**可选参数，用于指定日期。
*   **$Year：**可选参数，用于指定年份。
*   **$is_dst：**这是一个可选参数，如果时间在夏令时(DST)期间，则可以设置为 1；如果不是夏令时，则可以设置为 0。

**返回值：**此函数成功时返回整数 Unix 时间戳，错误时返回 False。

**异常：**如果使用$IS_DST 参数，则 PHP 5.3.0 版本会抛出 E_Deposated 错误。

下面的程序演示了 PHP 中的 gmmktime()函数：

**程序 1：**

```
<?php

// Using gmmktime() function to know the day
echo "August 30, 2018 was on "
. date("l", gmmktime(0, 0, 0, 8, 30, 2018));
?>
```

**Output:**

```
August 30, 2018 was on Thursday

```

**程序 2：**

```
<?php
// Using gmmktime() function to know
// the complete date
echo date("M-d-Y", gmmktime(0, 0, 0, 12, 1, 2012)) 
        . "<br>";

// Using gmmktime() function to know the
// complete date for an out-of-range input
echo date("M-d-Y", gmmktime(0, 0, 0, 12, 20, 2017));
?>
```

**Output:**

```
Dec-01-2012
Dec-20-2017

```

**相关文章：**

*   [PHP|mktime()函数](https://www.geeksforgeeks.org/php-mktime-function/)
*   [PHP|localtime()函数](https://www.geeksforgeeks.org/php-localtime-function/)
*   [PHP|date_sunset()函数](https://www.geeksforgeeks.org/php-date_sunset-function/)

**引用：**[http://php.net/manual/en/function.gmmktime.php](http://php.net/manual/en/function.gmmktime.php)