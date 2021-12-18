# 在 PHP 中比较两个日期

> 原文:[https://www.geeksforgeeks.org/comparing-two-dates-in-php/](https://www.geeksforgeeks.org/comparing-two-dates-in-php/)

给定两个日期(日期 1 和日期 2)，任务是比较给定的日期。当两个日期的格式相同时，在 PHP 中比较两个日期很简单，但是当两个日期的格式不同时，问题就出现了。

**方法 1:** 如果给定日期的格式相同，则使用简单的比较运算符来比较日期。

**例:**

```php
<?php
// PHP program to compare dates

// Declare two dates and 
// initialize it
$date1 = "1998-11-24";
$date2 = "1997-03-26";

// Use comparison operator to 
// compare dates
if ($date1 > $date2)
    echo "$date1 is latest than $date2";
else
    echo "$date1 is older than $date2";

?>
```

**输出:**

```php
1998-11-24 is latest than 1997-03-26

```

**方法 2:** 如果两个给定日期的格式不同，则使用 [strtotime()函数](https://www.geeksforgeeks.org/php-strtotime-function/)将给定日期转换为相应的时间戳格式，最后比较这些数字时间戳以获得所需的结果。

**例:**

```php
<?php
// PHP program to compare dates

// Declare two dates in different
// format
$date1 = "12-03-26";
$date2 = "2011-10-24";

// Use strtotime() function to convert
// date into dateTimestamp
$dateTimestamp1 = strtotime($date1);
$dateTimestamp2 = strtotime($date2);

// Compare the timestamp date 
if ($dateTimestamp1 > $dateTimestamp2)
    echo "$date1 is latest than $date2";
else
    echo "$date1 is older than $date2";

?>
```

**输出:**

```php
12-03-26 is latest than 2011-10-24

```

**方法 3:** 使用 DateTime 类比较两个日期。

**例:**

```php
<?php
// PHP program to compare dates

// Declare two dates in different
// format and use DateTime() function
// to convert date into DateTime
$date1 = new DateTime("12-11-24");
$date2 = new DateTime("2011-03-26");

// Compare the dates
if ($date1 > $date2)
    echo $date1->format("Y-m-d") . " is latest than "
            . $date2->format("Y-m-d");
else
    echo $date1->format("Y-m-d") . " is older than " 
            . $date2->format("Y-m-d");

?>
```

**输出:**

```php
2012-11-24 is latest than 2011-03-26

```

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。