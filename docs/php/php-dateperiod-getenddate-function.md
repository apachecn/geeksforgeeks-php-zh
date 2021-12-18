# PHP|DatePeriod getEndDate()函数

> Original: [https://www.geeksforgeeks.org/php-dateperiod-getenddate-function/](https://www.geeksforgeeks.org/php-dateperiod-getenddate-function/)

**DatePeriod：：getEndDate()函数**是 PHP 中的内置函数，用于返回结束日期。 如果给定的日期期间没有任何结束日期，则返回 NULL。
**语法：**和

```php
*DateTimeInterface* DatePeriod::getEndDate( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回给定日期段的结束日期。

以下程序说明 PHP：
**程序 1：**中的 DatePeriod：：getEndDate()函数

## PHP

```php
<?php

// Initialising a startDate with time
$StartDate = new DateTime('2019-09-30T00:00:00Z');

// Initialising a DateInterval of 2 day
$DateInterval = new DateInterval('P2D');

// Initialising a endDate with time
$EndDate = new DateTime('2019-10-02T00:00:00Z');

// Initialising a DatePeriod with startDate, DateInterval and
// endDate
$datePeriod = new DatePeriod( $StartDate, $DateInterval, $EndDate);

// Calling the getendDate() function
$endDate = $datePeriod->getEndDate();

// Getting the start date
echo $endDate->format(DateTime::ISO8601);
?>
```

**Output:** 

```php
2019-10-02T00:00:00+0000
```