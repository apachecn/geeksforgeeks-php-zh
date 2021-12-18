# 如何在 PHP 中给$Date 添加天数？

> 原文:[https://www . geesforgeks . org/how-to-add-days-date-in-PHP/](https://www.geeksforgeeks.org/how-to-add-days-to-date-in-php/)

向$Date 添加天数可以通过多种方式完成。在 PHP 中使用像 strtotime()，date_add()这样的内置函数是非常容易做到的。
**方法 1:** [**使用 strtotime()函数:**](https://www.geeksforgeeks.org/php-strtotime-function/)strtotime()函数用于将英文文本日期时间描述转换为 UNIX 时间戳。
**语法:**

```
strtotime( $EnglishDateTime, $time_now )
```

**参数:**该功能接受两个可选参数，如上所述，如下所述。

*   **$EnglishDateTime:** 此参数指定英文文本日期时间描述，表示要返回的日期或时间。
*   **$time_now:** 此参数指定用于计算返回值的时间戳。这是一个可选参数。

**程序:**用 strtotime()函数在 PHP 中给$Date 添加天数的 PHP 程序。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
// PHP program to add days to $Date

// Declare a date
$Date = "2019-05-10";

// Add days to date and display it
echo date('Y-m-d', strtotime($Date. ' + 10 days'));

?>
```

**Output:** 

```
2019-05-20
```

**方法二:** [**使用 date_add()函数:**](https://www.geeksforgeeks.org/php-date_create-date_format-add_date-functions/)date _ add()函数用于添加日、月、年、时、分、秒。
**语法:**

```
date_add(object, interval);
```

**参数:**该功能接受两个参数，如上所述，描述如下:

*   **对象:**指定 date_create()函数返回的 DateTime 对象。
*   **间隔:**指定 DateInterval 对象。

**程序:** PHP 程序使用 date_add()函数在 PHP 中给$Date 添加天数。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
// PHP program to add 10 days in date

// Declare a date
$date = date_create("2019-05-10");

// Use date_add() function to add date object
date_add($date, date_interval_create_from_date_string("10 days"));

// Display the added date
echo date_format($date, "Y-m-d");

?>
```

**Output:** 

```
2019-05-20
```