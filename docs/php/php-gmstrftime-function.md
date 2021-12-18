# PHP|gmstrftime()函数

> Original: [https://www.geeksforgeeks.org/php-gmstrftime-function/](https://www.geeksforgeeks.org/php-gmstrftime-function/)

Gmstrftime()函数是 PHP 中的内置函数，用于根据本地设置格式化 GMT/UTC 时间/日期。 PHP 中的 gmstrftime()函数与 strftime()的行为方式相同，只是 gmstrftime()函数返回的时间是格林威治标准时间(GMT)。 *$Format*和*$TimeZone*作为参数发送给 gmstrftime()函数，并返回根据使用给定时间戳指定的格式格式化的字符串。

**语法：**

```
string gmstrftime( $format, $timestamp )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$format:** required parameter to specify the format of the result.
*   **$TIMESTAMP:** this is an optional parameter that specifies the UNIX timestamp that represents the date and / or time to format.

**返回值：**此函数根据给定时间戳指定的格式返回格式化字符串。

**例外：**

*   月份、工作日名称和其他与语言相关的字符串与使用 setlocale()函数设置的当前区域设置相关。
*   如果 gmstrftime()函数中没有给出时间戳，它将缺省为 time()的值，换句话说就是当前本地时间。

以下程序说明了 PHP 中的 gmstrftime()函数：

**程序 1：**

```
<?php

// Using gmstrftime() function to return the GMT time
echo(gmstrftime("%B %d %Y, %X %Z", mktime(14, 0, 0, 8, 31, 18)));
?>
```

**输出：**

```
August 31 2018, 14:00:00 GMT

```

**程序 2：**

```
<?php

// Using gmstrftime() function to return the GMT time
setlocale(LC_ALL, 'en_US');
echo(gmstrftime("%B %d %Y, %X %Z"));
?>
```

**输出：**

```
August 31 2018, 09:55:21 GMT

```

**相关文章：**

*   [php|strtoTime()函数](https://www.geeksforgeeks.org/php-strtotime-function/)
*   [php|strpTime()函数](https://www.geeksforgeeks.org/php-strptime-function/)

**引用：**[http://php.net/manual/en/function.gmstrftime.php](http://php.net/manual/en/function.gmstrftime.php)