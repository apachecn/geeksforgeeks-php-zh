# PHP|Idate()函数

> Original: [https://www.geeksforgeeks.org/php-idate-function/](https://www.geeksforgeeks.org/php-idate-function/)

Idate()函数是 PHP 中的内置函数，用于将本地时间/日期格式化为整数。 $FORMAT 和$TIMESTAMP 作为参数发送给 Idate()函数，它返回一个使用给定时间戳按照指定格式格式化的整数。 与函数 date()不同，Idate()在格式参数中只接受一个字符。

**语法：**

```
int idate( $format, $timestamp )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$FORMAT：**这是一个必选参数，用于指定结果的格式。 Format 参数可以具有下列值：
    *   B-Swatch 节拍/上网时间
    *   D-每月的第几天
    *   小时(12 小时格式)
    *   小时(24 小时格式)
    *   这本书的记录
    *   I-如果激活了 DST(夏令时)，则返回 1，否则返回 0
    *   L-表示闰年返回 1，否则返回 0
    *   M 月数字
    *   秒-秒
    *   本月 T-天数
    *   Unix 时代以来的 U 秒(1970 年 1 月 1 日格林尼治标准时间 00：00：00)
    *   W-星期几(星期日=0)
    *   W-ISO-8601 周年号(周从周一开始)
    *   年(1 位或 2 位)
    *   年(4 位数字)
    *   一年中的 Z 日
    *   Z-时区偏移(秒)
*   **$timeStamp：**它是一个可选参数，指定代表要格式化的日期/时间的 Unix 时间戳。

**返回值：**它使用给定的时间戳按照指定的格式返回整数值。

**例外：**

*   如果时区无效，则 Idate()函数在每次调用日期/时间时抛出 E_Notify。
*   如果使用系统设置或 TZ 环境变量，则 Idate()函数抛出 E_STRICT 或 E_WARNING 消息。

下面的程序演示了 PHP 中的 Idate()函数：

**程序 1：**

```
<?php

// Formatting local date/time as Year
echo idate("Y") . "<br>";

// Formatting local date/time as Hour(24 hr format)
echo idate("H") . "<br>";

// Formatting local date/time as Minutes
echo idate("i") . "<br>";

// Formatting local date/time as day of the year 
echo idate("z") . "<br>";
?>
```

**Output:**

```
2018
11
22
238

```

**程序 2：**

```
<?php

// Parsing English textual datetime description into a Unix timestamp
$timestamp = strtotime('24th August 2018'); 

// Formatting local date/time as Year
echo idate('Y', $timestamp);
?>
```

**Output:**

```
2018

```

**相关文章：**

*   [PHP|time()函数](https://www.geeksforgeeks.org/php-time-function/)
*   [PHP|strptime()函数](https://www.geeksforgeeks.org/php-strptime-function/)

**引用：**[http://php.net/manual/en/function.idate.php](http://php.net/manual/en/function.idate.php)