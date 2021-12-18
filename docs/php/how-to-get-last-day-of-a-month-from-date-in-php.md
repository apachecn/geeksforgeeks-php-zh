# PHP 中如何从日期中获取一个月的最后一天？

> 原文:[https://www . geesforgeks . org/如何从 php 中的日期获取每月的最后一天/](https://www.geeksforgeeks.org/how-to-get-last-day-of-a-month-from-date-in-php/)

给定日期，任务是打印每月的最后一天。我们将使用 date()和 strtotime()函数来获取一个月的最后一天。

**使用的 PHP 函数:**

*   **[日期()功能:](https://www.geeksforgeeks.org/php-date-time/)** 格式化本地时间/日期。
*   **[strtotime()函数:](https://www.geeksforgeeks.org/php-strtotime-function/)** 将任何英文文本日期时间描述解析为一个 Unix 时间戳。

**示例:**

```
Input: 2020-04-23
Output: Thursday

Input: '2018-09-11'
Output: Sunday
```

**进场:**

*   给定以字符串形式存储在变量中的日期，步骤是使用 strtotime()函数将其转换为日期格式。
*   一旦我们得到日期，我们将使用 date()方法。
    **语法:**

    ```
    date( $format, $timestamp )
    ```

*   在$格式内，我们将传递“Y-m-t”，在$时间戳内传递上面的日期。在日期方面，“Y”用 4 位数给出一年的完整数字表示，“m”提供一个月的数字表示，“t”给出给定月份的天数。
*   通过使用“Y-m-t”，我们将获得一个月中的天数，因为“t”、“m”和“Y”将提供月份和年份。
*   最后一步是再次使用带有“l”格式的 date()，并将上面获得的日期作为$timestamp。
*   显示日期。

**程序:**

```
<?php

// Given a date in string format 
$datestring = '2020-04-23';

// Converting string to date
$date = strtotime($datestring);

// Last date of current month.
$lastdate = strtotime(date("Y-m-t", $date ));

// Day of the last date 
$day = date("l", $lastdate);

echo $day;
?>
```

**Output:**

```
Thursday

```