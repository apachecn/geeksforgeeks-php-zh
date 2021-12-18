# PHP|TIMEZONE_NAME_FROM_ABBR()函数

> Original: [https://www.geeksforgeeks.org/php-timezone_name_from_abbr-function/](https://www.geeksforgeeks.org/php-timezone_name_from_abbr-function/)

函数的作用是：在 PHP 中内置函数，用于返回缩写形式的时区名称。 缩写作为参数发送给 timezone_name_from_abbr()函数，如果成功则返回时区名称，如果失败则返回 False。

**语法：**

```
string timezone_name_from_abbr( $abbr, $gmtoffset, $isdst )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$abbr:** it is a required parameter for the specified time zone abbreviation.
*   **$gmtoffset:** this is an optional parameter that specifies the offset from GMT in seconds. The default value is-1, which returns the time zone corresponding to the first found abbr.
*   **$isdst:** specifies optional parameters for the daylight saving time indicator. The default value is-1, which means that daylight saving time is not considered in the time zone when searching.

**返回值：**成功时返回时区名称，失败时返回 False。

**异常：**timezone_name_from_abbr()函数是 DateTimeZone：：listAbbreviations 函数的别名。

下面的程序演示了 PHP 中的 timezone_name_from_abbr()函数：

**程序 1：**

```
<?php

// Displaying the name of timezone using the abbreviation
$abbr = timezone_name_from_abbr("PST");
echo ("PST stands for " . $abbr);
?>
```

**输出：**

```
PST stands for America/Los_Angeles

```

**程序 2：**

```
<?php

// Displaying the name of timezone using the abbreviation
$abbr = timezone_name_from_abbr("", 7200, 0);
echo ("The given parameter stands for " . $abbr);
?>
```

**输出：**

```
The given parameter stands for Europe/Helsinki

```

**相关文章：**

*   [PHP|TIMEZONE_OPEN()11-13](https://www.geeksforgeeks.org/php-timezone_open-function/)
*   [PHP|TIMEZONE_VERSION_GET()11-13](https://www.geeksforgeeks.org/php-timezone_version_get-function/)

**引用：**[http://php.net/manual/en/function.timezone-name-from-abbr.php](http://php.net/manual/en/function.timezone-name-from-abbr.php)