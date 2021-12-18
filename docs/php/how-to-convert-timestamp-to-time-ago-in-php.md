# PHP 中如何将时间戳转换为时间前？

> 原文:[https://www . geesforgeks . org/如何将时间戳转换为 php 中的时间前/](https://www.geeksforgeeks.org/how-to-convert-timestamp-to-time-ago-in-php/)

给定时间，任务是将时间戳转换为以前的时间。以前的格式消除了不同时区转换的问题。下面给出了一个进行时间转换的函数。在这个函数中，将时间戳作为输入，然后从当前时间戳中减去它，将其转换为以前的时间格式。要实现这个功能，需要定义一些规则，从减法后的剩余日期中确定年、月、日、分等。

**例 1:**

```php
<?php
// PHP program to convert timestamp
// to time ago

function time_Ago($time) {

    // Calculate difference between current
    // time and given timestamp in seconds
    $diff     = time() - $time;

    // Time difference in seconds
    $sec     = $diff;

    // Convert time difference in minutes
    $min     = round($diff / 60 );

    // Convert time difference in hours
    $hrs     = round($diff / 3600);

    // Convert time difference in days
    $days     = round($diff / 86400 );

    // Convert time difference in weeks
    $weeks     = round($diff / 604800);

    // Convert time difference in months
    $mnths     = round($diff / 2600640 );

    // Convert time difference in years
    $yrs     = round($diff / 31207680 );

    // Check for seconds
    if($sec <= 60) {
        echo "$sec seconds ago";
    }

    // Check for minutes
    else if($min <= 60) {
        if($min==1) {
            echo "one minute ago";
        }
        else {
            echo "$min minutes ago";
        }
    }

    // Check for hours
    else if($hrs <= 24) {
        if($hrs == 1) { 
            echo "an hour ago";
        }
        else {
            echo "$hrs hours ago";
        }
    }

    // Check for days
    else if($days <= 7) {
        if($days == 1) {
            echo "Yesterday";
        }
        else {
            echo "$days days ago";
        }
    }

    // Check for weeks
    else if($weeks <= 4.3) {
        if($weeks == 1) {
            echo "a week ago";
        }
        else {
            echo "$weeks weeks ago";
        }
    }

    // Check for months
    else if($mnths <= 12) {
        if($mnths == 1) {
            echo "a month ago";
        }
        else {
            echo "$mnths months ago";
        }
    }

    // Check for years
    else {
        if($yrs == 1) {
            echo "one year ago";
        }
        else {
            echo "$yrs years ago";
        }
    }
}

// Initialize current time
$curr_time = "2013-07-10 09:09:09";

// The strtotime() function converts
// English textual date-time
// description to a UNIX timestamp.
$time_ago = strtotime($curr_time);

// Display the time ago
echo time_Ago($time_ago) . "\n";

// Initialize current time
$curr_time="2019-01-05 09:09:09";

// The strtotime() function converts
// English textual date-time
// description to a UNIX timestamp.
$time_ago =strtotime($curr_time);

// Display the time ago
echo time_Ago($time_ago);
?>
```

**Output:**

```php
6 years ago
5 days ago

```

**例 2:**

```php
<?php
// PHP program to convert timestamp
// to time ago

function to_time_ago( $time ) {

    // Calculate difference between current
    // time and given timestamp in seconds
    $diff = time() - $time;

    if( $diff < 1 ) { 
        return 'less than 1 second ago'; 
    }

    $time_rules = array ( 
                12 * 30 * 24 * 60 * 60 => 'year',
                30 * 24 * 60 * 60       => 'month',
                24 * 60 * 60           => 'day',
                60 * 60                   => 'hour',
                60                       => 'minute',
                1                       => 'second'
    );

    foreach( $time_rules as $secs => $str ) {

        $div = $diff / $secs;

        if( $div >= 1 ) {

            $t = round( $div );

            return $t . ' ' . $str . 
                ( $t > 1 ? 's' : '' ) . ' ago';
        }
    }
}

// to_time_ago() function call
echo to_time_ago( time() - 5);

?>
```

**Output:**

```php
5 seconds ago

```