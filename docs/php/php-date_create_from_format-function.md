# PHP|DATE_CREATE_FROM_FORMAT()函数

> Original: [https://www.geeksforgeeks.org/php-date_create_from_format-function/](https://www.geeksforgeeks.org/php-date_create_from_format-function/)

DATE_CREATE_FROM_FORMAT()是 php 中的一个内置函数，用于根据指定的格式解析时间字符串。 此函数接受三个参数，成功时返回新的 DateTime，失败时返回 False。

**语法：**
过程化风格

```php
date_create_from_format ( $format, $time, $timezone )
```

面向对象的样式

```php
DateTime::createFromFormat ( $format, $time, $timezone )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$FORMAT：**日期格式是必选参数，用于指定日期格式。 格式中使用了以下参数字符串。
    1.  **日期：**
        *   **d 和 j：**月份的第几天，带或不带前导零的 2 位数字。
        *   **d 和 l：**一天的文本表示。
        *   **S：**月中日期的英文序号后缀，2 个字符。 它在处理时被忽略。
        *   **z：**一年中的第几天(从 0 开始)
    2.  **月份：**
        *   **F 和 M：**月份的文本表示形式，如 1 月或 9 月
        *   **m 和 n：**月份的数字表示形式，带或不带前导零
    3.  **年份：**
        *   **Y：**年份的完整数字表示，4 位
        *   **y：**年份的两位数表示法(假定在 1970-2069(含 1970-2069)范围内)
    4.  **时间：**
        *   **A 和 A：**经脉前后
        *   **g 和 h：**12 小时格式，包含或不包含前导零
        *   **G 和 H：**24 小时格式，带或不带前导零
        *   **i：**分钟，前导为零
        *   **s：**秒，前导零
        *   **u：**微秒(最多六位)
    5.  **时区：**
        *   **E、O、P 和 T：**时区标识符，或与 UTC 的小时差，或与 UTC 的差，小时和分钟之间的冒号，或时区缩写
    6.  **完整日期/时间：**
        *   **u：**秒，自 Unix 时代(1970 年 1 月 1 日 00：00：00 GMT)
    7.  **空格和分隔符：**
        *   **(空格)：**一个空格或一个制表符
        *   **#：**以下分隔符之一：；、：、/、.、-、(或)
        *   **；、：、/、.、-、(Or)：**指定字符。
        *   **？：**随机字节
        *   ***：**直到下一个分隔符或数字的随机字节
        *   **！：**将所有字段(年、月、日、小时、分钟、秒、分数和时区信息)重置为 Unix 纪元
        *   **|：**如果所有字段(年、月、日、小时、分钟、秒、分数和时区信息)尚未解析，则将其重置为 Unix 纪元
        *   **+：**如果存在此格式说明符，则字符串中的尾随数据不会导致错误，而是会发出警告
*   **$time：**此参数用作表示时间的字符串。
*   **$timeZone：**此参数用作表示所需时区的 DateTimeZone 对象。

**返回值：**此函数成功时返回新的 DateTime 实例，失败时返回 False。

下面的程序演示了 PHP 中的 date_create_from_format()函数。

**程序 1：**

```php
<?php

// Declare a date in given format
$date = date_create_from_format('D-M-Y', 'monday-Feb-2018');

// Output date in given format
echo date_format($date, 'y-n-j');
?>
```

**Output:**

```php
18-2-5

```

**程序 2：**

```php
<?php

// Declare a date in given format
$date = DateTime::createFromFormat('D-M-Y', 'monday-Feb-2018');

// Output date in given format
echo $date->format('Y-m-d');
?>
```

**Output:**

```php
2018-02-05

```

**引用：**[http://php.net/manual/en/datetime.createfromformat.php](http://php.net/manual/en/datetime.createfromformat.php)