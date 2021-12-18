# PHP 中如何计算一个数组的总时间？

> 原文:[https://www . geeksforgeeks . org/如何计算 php 中的数组总时间/](https://www.geeksforgeeks.org/how-to-calculate-total-time-of-an-array-in-php/)

给定一个包含时间的数组，格式为 hr:min:sec。任务是计算总时间。如果总时间大于 24 小时，则总时间不会从 0 开始。它将显示总时间。从数组中计算总时间有两种方法。

1.  Use strtotime () function
2.  Use the explode () function.

**使用 [strtotime()函数](https://www.geeksforgeeks.org/php-strtotime-function/):**strtotime()函数用于将字符串转换为时间格式。该函数以 h:m:s 格式返回时间。

**语法**

```php
strtotime( string )
```

**示例 1:** 本示例从数组中读取值，并将其转换为时间格式。

```php
<?php

// Array containing time in string format
$time = [ 
    '00:04:35', '00:02:06', '01:09:12',
    '09:19:04', '00:17:49', '02:13:59',
    '10:10:54' 
];

$sum = strtotime('00:00:00');

$totaltime = 0;

foreach( $time as $element ) {

    // Converting the time into seconds
    $timeinsec = strtotime($element) - $sum;

    // Sum the time with previous value
    $totaltime = $totaltime + $timeinsec;
}

// Totaltime is the summation of all
// time in seconds

// Hours is obtained by dividing
// totaltime with 3600
$h = intval($totaltime / 3600);

$totaltime = $totaltime - ($h * 3600);

// Minutes is obtained by dividing
// remaining total time with 60
$m = intval($totaltime / 60);

// Remaining value is seconds
$s = $totaltime - ($m * 60);

// Printing the result
echo ("$h:$m:$s");

?>
```

**输出:**

```php
23:17:39

```