# PHP|date_create_immutable_from_format()函数

> Original: [https://www.geeksforgeeks.org/php-date_create_immutable_from_format-function/](https://www.geeksforgeeks.org/php-date_create_immutable_from_format-function/)

**DATE_CREATE_IMMUTABLE_FROM_FORMAT()函数**是 PHP 中的内置函数，用于根据指定的格式解析时间字符串。

**语法：**

*   面向对象的样式：

```php
*DateTimeImmutable* static DateTime::createFromFormat( *string* $format,
                                      *string* $time, *DateTimeZone* $timezone )
```

*   程序风格：

```php
*DateTimeImmutable* date_create_from_format( *string* $format, 
                                      *string* $time, *DateTimeZone* $timezone )
```

**参数：**此函数使用上述三个参数，如下所述：

*   **$format：**此参数以字符串形式保存日期时间格式。
*   **$time：**此参数以字符串格式保存时间。
*   **$timeZone：**此参数保存 DateTimeZone 对象。

**返回值：**此函数返回一个新的 DateTimeImmutable 对象，该对象表示由时间字符串指定的日期和时间，该时间字符串的格式为给定的格式。

**字符及其说明：**

<figure class="table">

| 格式化字符 | 描述 / 描写 / 形容 / 类别 | 示例返回值 |
| --- | --- | --- |
| 虚量 / 相当于－1 的平方根 | 不带前导零的月份的第几天 | 1 至 31 |
| 双角动量的 / 女儿 / 一天 / 白天 | 带有前导零的月份的第几天 | 01 至 31 |
| 米 / 模 / 毫 / 兆 | 月份的数字表示形式 | 01 至 12 |
| 兆 / 模 / 毫 / 米 | 月份的简短文本表示法 | 1 月至 12 月 |
| 英语字母表中第二十五个字母 / Y 字形 / Y 项 | 一年的代表权 | 1989、2017 |

</figure>

格式字符串可以是任意顺序的任何格式字符的组合，但是我们必须以相同的顺序提供输入日期-时间字符串。

下面的程序演示了 PHP 中的 date_create_immutable_from_format()函数：

**程序 1：**

## PHP

```php
<?php

// Use date_create_from_format() function
// to create a date format
$date = date_create_from_format('j-M-Y', '03-oct-2019');

// Display the date
echo date_format($date, 'Y-m-d');

?>
```

**Output:** 

```php
2019-10-03
```

**程序 2：**

## PHP

```php
<?php

// Use date_create_from_format() function
// to create a date format
$date = date_create_from_format('d-M-Y', '03-oct-2019');

// Display the date
echo date_format($date, 'Y-m-j');

?>
```

**Output:** 

```php
2019-10-3
```

**程序 3：**

## PHP

```php
<?php

// Use DateTime::createFromFormat() function
// to create a date object
$date = DateTime::createFromFormat('j-M-Y', '03-oct-2019');

// Display the date
echo $date->format('Y-m-d');

?>
```

**Output:** 

```php
2019-10-03
```

**引用：**[https://www.php.net/manual/en/datetimeimmutable.createfromformat.php](https://www.php.net/manual/en/datetimeimmutable.createfromformat.php)