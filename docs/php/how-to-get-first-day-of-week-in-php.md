# PHP 中如何获取一周的第一天？

> 原文:[https://www . geeksforgeeks . org/如何获得 php 中的每周第一天/](https://www.geeksforgeeks.org/how-to-get-first-day-of-week-in-php/)

使用 [strtotime()函数](https://www.geeksforgeeks.org/php-strtotime-function/)使用 PHP 获取一周的第一天。该函数返回默认的时间变量 timestamp，然后使用 date()函数将时间戳日期转换为可理解的日期。

**strtotime()函数:**strtotime()函数通过解析时间字符串返回时间戳中的结果。
**语法:**

```php
strtotime($EnglishDateTime, $time_now)
```

**参数:**strtotime()函数接受两个参数，如上所述，如下所述:

*   **$EnglishDateTime:** 它指定英文文本日期时间描述，表示要返回的日期或时间。该函数解析字符串并返回以秒为单位的时间。它是必需的参数。
*   **$time_now:** 此参数指定用于计算返回值的时间戳。这是一个可选参数。

**date()函数:**date()函数返回更容易理解和人类可读的日期格式。
**语法:**

```php
date( format, timestamp )
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **格式:**指定显示结果的日期和时间格式。
*   **时间戳:**是生成日期的默认时间变量。

**注意:**在 PHP 中，一周从星期一开始，所以如果时间字符串被给定为“本周”，输出将是星期一的时间戳，通过 date()函数可以使其可读。

**程序 1:** 当时间字符串为“本周”时，获取默认的一周第一天。

```php
<?php

// PHP program to print default first
// day of current week

// l will display the name of the day

// d, m, Y will display the day, month
// and year respectively 
$firstday = date('l - d/m/Y', strtotime("this week"));

echo "First day of this week: ", $firstday;

?>
```

**Output:**

```php
First day of this week: Monday - 04/02/2019

```

现在，通常星期天被认为是一周的第一天。因此，在 PHP 中，要将周日作为一周的第一天，请考虑前一周的周日。即得到一周的第一天(星期日)需要得到前一周的星期日和得到下周的第一天(星期日)需要得到本周的星期日等等。
PHP 支持时间字符串中的-ve 索引。因此，为了获得前一周，它可以使用时间字符串作为“-1 周”，为了获得一天，它还必须在时间字符串中包含一天的名称。

**程序 2:** 获取一周的第一天(周日)。

```php
<?php

// PHP program to display sunday as first day of a week

// l will display the name of the day
// d, m and Y will display the day, month and year respectively

// For current week the time-string will be "sunday -1 week"
// here -1 denotes last week
$firstday = date('l - d/m/Y', strtotime("sunday -1 week"));
echo "First day of this week: ", $firstday, "\n";

// For previous week the time-string wil be "sunday -2 week"
// here -2 denotes week before last week
$firstday = date('l - d/m/Y', strtotime("sunday -2 week"));
echo "First day of last week: ", $firstday, "\n";

// For next week the time-string wil be "sunday 0 week"
// here 0 denotes this week
$firstday = date('l - d/m/Y', strtotime("sunday 0 week"));
echo "First day of next week: ", $firstday, "\n";

// For week after next week the time-string wil be "sunday 1 week"
// here 1 denotes next week
$firstday = date('l - d/m/Y', strtotime("sunday 1 week"));
echo "First day of week after next week : ", $firstday;

?>
```

**Output:**

```php
First day of this week: Sunday - 03/02/2019
First day of last week: Sunday - 27/01/2019
First day of next week: Sunday - 10/02/2019
First day of week after next week : Sunday - 17/02/2019

```