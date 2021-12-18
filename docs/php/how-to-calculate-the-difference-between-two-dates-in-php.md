# PHP 中如何计算两个日期的差值？

> 原文:[https://www . geesforgeks . org/如何用 php 计算两个日期之间的差异/](https://www.geeksforgeeks.org/how-to-calculate-the-difference-between-two-dates-in-php/)

在本文中，我们将看到如何在 PHP 中计算两个日期之间的差异，并通过示例了解其实现。给定两个日期。，start_date 和 end_date &我们需要找出这两个日期之间的区别。

**考虑下面的例子:**

```
Input: start_date: 2016-06-01 22:45:00 
       end_date: 2018-09-21 10:44:01
Output: 2 years, 3 months, 21 days, 11 hours, 59 minutes, 1 seconds
Explanation: The difference of 2 dates will give the date in complete format.
```

**方法 1:** **使用** [**date_diff()函数**](https://www.geeksforgeeks.org/php-date_diff-function/)

该函数用于查找两个日期之间的差异。该函数将在成功时返回一个 DateInterval 对象，在失败时返回 FALSE。

**示例**:本示例说明了使用 date_diff()函数计算两个日期之间的差异。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

  // Creates DateTime objects
  $datetime1 = date_create('2016-06-01');
  $datetime2 = date_create('2018-09-21');

  // Calculates the difference between DateTime objects
  $interval = date_diff($datetime1, $datetime2);

  // Printing result in years & months format
  echo $interval->format('%R%y years %m months');
?>
```

**输出:**

```
+2 years 3 months
```

**方法二:**用日期时间数学公式求两个日期的差。它返回两个指定日期之间的年、月、日、小时、分钟、秒。

**示例:**在本例中，我们将使用日期-时间数学公式来计算以年、月、日、小时、分钟、秒为单位返回的日期之间的差异。

## PHP

```
<?php

  // Declare and define two dates
  $date1 = strtotime("2016-06-01 22:45:00");
  $date2 = strtotime("2018-09-21 10:44:01");

  // Formulate the Difference between two dates
  $diff = abs($date2 - $date1);

  // To get the year divide the resultant date into
  // total seconds in a year (365*60*60*24)
  $years = floor($diff / (365*60*60*24));

  // To get the month, subtract it with years and
  // divide the resultant date into
  // total seconds in a month (30*60*60*24)
  $months = floor(($diff - $years * 365*60*60*24)
                                 / (30*60*60*24));

  // To get the day, subtract it with years and
  // months and divide the resultant date into
  // total seconds in a days (60*60*24)
  $days = floor(($diff - $years * 365*60*60*24 -
               $months*30*60*60*24)/ (60*60*24));

  // To get the hour, subtract it with years,
  // months & seconds and divide the resultant
  // date into total seconds in a hours (60*60)
  $hours = floor(($diff - $years * 365*60*60*24
         - $months*30*60*60*24 - $days*60*60*24)
                                     / (60*60));

  // To get the minutes, subtract it with years,
  // months, seconds and hours and divide the
  // resultant date into total seconds i.e. 60
  $minutes = floor(($diff - $years * 365*60*60*24
           - $months*30*60*60*24 - $days*60*60*24
                            - $hours*60*60)/ 60);

  // To get the minutes, subtract it with years,
  // months, seconds, hours and minutes
  $seconds = floor(($diff - $years * 365*60*60*24
           - $months*30*60*60*24 - $days*60*60*24
                  - $hours*60*60 - $minutes*60));

  // Print the result
  printf("%d years, %d months, %d days, %d hours, "
       . "%d minutes, %d seconds", $years, $months,
               $days, $hours, $minutes, $seconds);
?>
```

**输出:**

```
2 years, 3 months, 21 days, 11 hours, 59 minutes, 1 seconds
```

**方法 3:** 此方法用于获取两个指定日期之间的总天数。

## PHP

```
<?php

  // Declare two dates
  $start_date = strtotime("2018-06-08");
  $end_date = strtotime("2018-09-19");

  // Get the difference and divide into
  // total no. seconds 60/60/24 to get
  // number of days
  echo "Difference between two dates: "
      . ($end_date - $start_date)/60/60/24;
?>
```

**输出:**

```
Difference between two dates: 103
```

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。