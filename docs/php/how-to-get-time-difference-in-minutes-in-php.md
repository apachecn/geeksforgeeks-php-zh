# PHP 中如何获取分钟时差？

> 原文:[https://www . geesforgeks . org/如何获得 php 中的分钟时差/](https://www.geeksforgeeks.org/how-to-get-time-difference-in-minutes-in-php/)

在本文中，我们将学习如何使用 PHP 获取以分钟为单位的时差。

我们将使用内置功能[**date _ diff()**](https://www.geeksforgeeks.org/php-date_diff-function/)**到获取以分钟为单位的时差。为此，我们需要一个开始日期和结束日期来使用 **date_diff()** 函数计算它们的时差(以分钟为单位)。**

****语法:****

```php
date_diff($datetime1, $datetime2);
```

****参数:****date _ diff()**函数接受两个参数，如上所述，如下所述。**

*   ****$datetime1:** 这是一个强制参数，因为它指定了开始/第一个 datetime 对象。**
*   ****$datetime2:** 这是一个强制参数，因为它指定了结束/第二个 datetime 对象。**

****返回值:**该函数返回第一个日期时间对象和第二个日期时间对象之间的差值，否则在失败时返回*假*。**

****例 1:** 下面的程序说明了 **date_diff()** 函数获取分钟的时间差。**

## **服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**

```php
<?php 
// PHP Program to illustrate
//date_diff() function

// Creating DateTime Objects
$dateTimeObject1 = date_create('2019-05-18'); 
$dateTimeObject2 = date_create('2020-05-18'); 

// Calculating the difference between DateTime Objects
$interval = date_diff($dateTimeObject1, $dateTimeObject2); 
echo ("Difference in days is: ");

// Printing the result in days format
echo $interval->format('%R%a days');
echo "\n<br/>";
$min = $interval->days * 24 * 60;
$min += $interval->h * 60;
$min += $interval->i;

// Printing the Result in Minutes format.
echo("Difference in minutes is: ");
echo $min.' minutes';
?>
```

****输出:****

```php
Difference in days is: +366 days
Difference in minutes is: 527040 minutes
```

****例 2:****

## **服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**

```php
<?php 
  // PHP Program to illustrate
  // date_diff() function

  // Creating DateTime Objects
  $dateTimeObject1 = date_create('2020-05-14'); 
  $dateTimeObject2 = date_create('2021-02-14'); 

  // Calculating the difference between DateTime Objects
  $interval = date_diff($dateTimeObject1, $dateTimeObject2); 
  echo ("Difference in days is: ");

  // Printing the result in days format
  echo $interval->format('%R%a days');
  echo "\n<br/>";
  $min = $interval->days * 24 * 60;
  $min += $interval->h * 60;
  $min += $interval->i;

  // Printing the Result in Minutes format.
  echo("Difference in minutes is: ");
  echo $min.' minutes';
?>
```

****输出:****

```php
Difference in days is: +276 days
Difference in minutes is: 397440 minutes
```

****例 3:****

## **服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**

```php
<?php 
// PHP program to illustrate 
// date_diff() function

// Creating DateTime objects
$dateTimeObject1 = date_create('19:15:00'); 
$dateTimeObject2 = date_create('12:15:00'); 

// Calculating the difference between DateTime objects
$interval = date_diff($dateTimeObject1, $dateTimeObject2); 

// Printing result in hours
echo ("Difference in hours is:");
echo $interval->h;
echo "\n<br/>";
$minutes = $interval->days * 24 * 60;
$minutes += $interval->h * 60;
$minutes += $interval->i;

//Printing result in minutes
echo("Difference in minutes is:");
echo $minutes.' minutes';
?>
```

****输出:****

```php
Difference in hours is:7
Difference in minutes is:420 minutes
```