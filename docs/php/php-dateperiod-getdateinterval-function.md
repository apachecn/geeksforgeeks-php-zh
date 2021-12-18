# PHP|DatePeriod getDateInterval()函数

> Original: [https://www.geeksforgeeks.org/php-dateperiod-getdateinterval-function/](https://www.geeksforgeeks.org/php-dateperiod-getdateinterval-function/)

**DatePeriod：：getDateInterval()函数**是 PHP 中的内置函数，用于返回给定日期段的日期间隔。

**语法：**

```
*DateInterval* DatePeriod::getDateInterval( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回给定日期段的 DateInterval 对象。

下面的程序演示了 PHP 中的 DatePeriod：：getDateInterval()函数：

**程序 1：**

```
<?php

// Create a new DatePeriod object
$DP = new DatePeriod('R7/2019-09-25T12:30:00Z/P5D');

// Calling the DatePeriod::getDateInterval() function
$dateInterval = $DP->getDateInterval();

// Getting the date interval of the given DatePeriod
echo $dateInterval->format('%d days');

?>
```

**输出：**

```
5 days

```

**程序 2：**

```
<?php

// Declare the start date
$start_date = new DateTime('2019-09-01');

// Declare the DateInterval
$interval = new DateInterval('P5D');

// Declare the end date
$end_date = new DateTime('2019-09-30');

// Create a new DatePeriod object
$DP = new DatePeriod($start_date, $interval, $end_date);

// Calling the DatePeriod::getDateInterval() function
$dateInterval = $DP->getDateInterval();

// Getting the date interval of the given DatePeriod
echo $dateInterval->format('%d days');

?>
```

**输出：**

```
5 days

```

**引用：**[https://www.php.net/manual/en/dateperiod.getdateinterval.php](https://www.php.net/manual/en/dateperiod.getdateinterval.php)