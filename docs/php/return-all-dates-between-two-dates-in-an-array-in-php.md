# 返回 PHP 中数组中两个日期之间的所有日期

> 原文:[https://www . geesforgeks . org/return-两个日期之间的所有日期-数组中的日期-php/](https://www.geeksforgeeks.org/return-all-dates-between-two-dates-in-an-array-in-php/)

给定两个日期(开始日期和结束日期)，任务是返回数组中的所有日期。

**示例 1:** 在此示例中，使用日期间隔类，该类以 DateTime 的格式存储固定时间量(以年、月、日、小时等为单位)或相对时间字符串。

```php
<?php

// Function to get all the dates in given range
function getDatesFromRange($start, $end, $format = 'Y-m-d') {

    // Declare an empty array
    $array = array();

    // Variable that store the date interval
    // of period 1 day
    $interval = new DateInterval('P1D');

    $realEnd = new DateTime($end);
    $realEnd->add($interval);

    $period = new DatePeriod(new DateTime($start), $interval, $realEnd);

    // Use loop to store date into array
    foreach($period as $date) {                 
        $array[] = $date->format($format); 
    }

    // Return the array elements
    return $array;
}

// Function call with passing the start date and end date
$Date = getDatesFromRange('2010-10-01', '2010-10-05');

var_dump($Date);

?>
```

**Output:**

```php
array(5) {
  [0]=>
  string(10) "2010-10-01"
  [1]=>
  string(10) "2010-10-02"
  [2]=>
  string(10) "2010-10-03"
  [3]=>
  string(10) "2010-10-04"
  [4]=>
  string(10) "2010-10-05"
}

```

**示例 2:** 本示例使用 [strtotime()函数](https://www.geeksforgeeks.org/php-strtotime-function/)，该函数用于将英文文本日期时间描述转换为 UNIX 时间戳。成功时返回时间戳，否则返回 False。

```php
<?php

// Declare two dates
$Date1 = '01-10-2010';
$Date2 = '05-10-2010';

// Declare an empty array
$array = array();

// Use strtotime function
$Variable1 = strtotime($Date1);
$Variable2 = strtotime($Date2);

// Use for loop to store dates into array
// 86400 sec = 24 hrs = 60*60*24 = 1 day
for ($currentDate = $Variable1; $currentDate <= $Variable2; 
                                $currentDate += (86400)) {

$Store = date('Y-m-d', $currentDate);
$array[] = $Store;
}

// Display the dates in array format
print_r($array);
?>
```

**Output:**

```php
Array
(
    [0] => 2010-10-01
    [1] => 2010-10-02
    [2] => 2010-10-03
    [3] => 2010-10-04
    [4] => 2010-10-05
)

```