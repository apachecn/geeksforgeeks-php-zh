# PHP|DatePeriod getStartDate()函数

> Original: [https://www.geeksforgeeks.org/php-dateperiod-getstartdate-function/](https://www.geeksforgeeks.org/php-dateperiod-getstartdate-function/)

**DatePeriod：：getStartDate()函数**是 PHP 中的内置函数，用于返回给定日期段的开始日期。

**语法：**

```
*DateTimeInterface* DatePeriod::getStartDate( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回给定日期段的开始日期。

下面的程序演示了 PHP 中的 DatePeriod：：getStartDate()函数：

**程序 1：**

```
<?php

// Initialising a startDate with time
$StartDate = new DateTime('2019-05-16T00:00:00Z');

// Initialising a DateInterval of 2 day
$DateInterval = new DateInterval('P2D');

// Initialising a endDate with time
$EndDate = new DateTime('2019-05-20T00:00:00Z');

// Initialising a DatePeriod with startDate, DateInterval and
// endDate 
$datePeriod = new DatePeriod( $StartDate, $DateInterval, $EndDate);

// Calling the getStartDate() function
$StartDate = $datePeriod->getStartDate();

// Getting the start date
echo $StartDate->format(DateTime::ISO8601);

?>
```

**输出：**

```
2019-05-16T00:00:00+0000

```

**程序 2：**

```
<?php

// Initialising a DatePeriod with a date of 2019-09-30,
// time of 10 hours, 40 minutes and 44 seconds and with
// day period of 14 days
$datePeriod = new DatePeriod('R7/2019-09-30T10:40:44Z/P14D');

// Calling the getStartDate() function
$StartDate = $datePeriod->getStartDate();

// Getting the start date
echo $StartDate->format(DateTime::ISO8601);
?>
```

**输出：**

```
2019-09-30T10:40:44+0000

```

**引用：**[https://www.php.net/manual/en/dateperiod.getstartdate.php](https://www.php.net/manual/en/dateperiod.getstartdate.php)