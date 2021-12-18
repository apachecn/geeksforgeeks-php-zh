# 在 PHP

中查找两个日期之间的天数的程序

> Original: [https://www.geeksforgeeks.org/program-to-find-the-number-of-days-between-two-dates-in-php/](https://www.geeksforgeeks.org/program-to-find-the-number-of-days-between-two-dates-in-php/)

在本文中，我们将了解如何在 PHP 中获取天数中的日期差异，同时还将了解获取两个日期中差异总数的各种方法，并通过示例查看它们的实现。 我们给出了两个日期&我们的任务是找出这两个给定日期之间的天数。 为此，我们将遵循以下两种方法：

*   Use the [**strtotime () function**](https://www.geeksforgeeks.org/php-strtotime-function/)
*   Use the [**date_diff () function**](https://www.geeksforgeeks.org/php-date_diff-function/)

**考虑以下示例：**

```php
Input : date1 = "2-05-2017"
        date2 = "25-12-2017"
Output: Difference between two dates: 237 Days
Explanation: Calculating the total number of days between the start & end date.
```

**注：**日期可以采用任何格式。 在上面的示例中，日期采用 dd-mm-yyyy 格式。

**方法 1：**[**使用 strtotime()函数**](https://www.geeksforgeeks.org/php-strtotime-function/)

这是 PHP 中的一个内置函数，用于将英文文本日期时间描述转换为 UNIX 时间戳。 该函数接受英语字符串参数，该参数表示日期-时间的描述。 例如，“Now”指的是英文日期-时间描述中的当前日期。 此函数返回自[Unix 纪元](https://en.wikipedia.org/wiki/Unix_time)以来的时间(以秒为单位)。

**示例 1：**在此示例中，我们获取了两个日期并计算了它们的差异。

## PHP

```php
<?php

  // Function to find the difference 
  // between two dates.
  function dateDiffInDays($date1, $date2) 
  {
      // Calculating the difference in timestamps
      $diff = strtotime($date2) - strtotime($date1);

      // 1 day = 24 hours
      // 24 * 60 * 60 = 86400 seconds
      return abs(round($diff / 86400));
  }

  // Start date
  $date1 = "17-09-2018";

  // End date
  $date2 = "31-09-2018";

  // Function call to find date difference
  $dateDiff = dateDiffInDays($date1, $date2);

  // Display the result
  printf("Difference between two dates: "
     . $dateDiff . " Days ");
?>
```

**输出：**和

```php
Difference between two dates: 14 Days
```

和

**方法 2：**[**使用 date_diff()函数**](https://www.geeksforgeeks.org/php-date_diff-function/)

Date_diff()函数是 PHP 中的一个内置函数，用于计算两个日期之间的差值。 此函数在成功时返回 DateInterval 对象，在失败时返回 False。

**示例：**此示例介绍如何在 PHP 中计算两个日期之间的天数。

## PHP

```php
<?php

  // Creates DateTime objects
  $datetime1 = date_create('17-09-2018');
  $datetime2 = date_create('25-09-2018');

  // Calculates the difference between DateTime objects
  $interval = date_diff($datetime1, $datetime2);

  // Display the result
  echo $interval->format('Difference between two dates: %R%a days');
?>
```

**输出：**和

```php
Difference between two dates: +8 days
```

和

PHP 是一种专门为 Web 开发设计的服务器端脚本语言。 您可以按照这个[PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和[PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。