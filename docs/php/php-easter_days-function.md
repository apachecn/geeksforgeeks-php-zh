# PHP|Easter_Days()函数

> Original: [https://www.geeksforgeeks.org/php-easter_days-function/](https://www.geeksforgeeks.org/php-easter_days-function/)

Easter_day()函数是 PHP 中的一个内置函数，它返回 3 月 21 日之后的天数，即复活节在给定的年份。 如果未指定年份，则将当前年份作为默认值。

**语法：**

```
easter_days( $year, $method )
```

**参数：**此函数接受两个可选参数，如下所示：

1.  **$Year** this parameter specifies the year. If no parameters are passed, the current year is taken as the default value.
2.  **$Method-** this parameter allows you to calculate the Easter date based on other calendars. If the *$method* is set to CAL_Easter_Roman, it uses the Gregorian calendar between 1582 and 1752.

**返回值：**此函数返回 3 月 21 日之后的天数，即复活节在给定年份。 如果未将**$Year**作为参数传递，则将当前年份作为默认年份，并返回当前年份 3 月 21 日之后的天数。

例如：

```
Input :  $year = 2018
Output : 11

Input : $year = 2017
Output : 26  

Input: $year = 2015 $method = CAL_EASTER_ROMAN
Output : 15  

```

以下程序说明了 Easter_Days()函数的用法：

**程序 1：**下面的程序解释了未传递参数时 Easter_Days()函数的工作原理。

```
<?php
// PHP program to demonstrate the 
// easter_days() function 
// when no parameter is passed 

echo easter_days(), "\n";  

// verified by passing current year
$year = 2018; 
echo easter_days($year);  
?>
```

帖子主题：Re：Колибри

**程序 2：**下面的程序解释了传递**$Year**参数

```
<?php
// PHP program to demonstrate the 
// easter_days() function 
// when $year parameter is passed 

$year = 2015; 

// no of days for Easter after march 21 of year 2015
echo easter_days($year), "\n";  

// the Easter date of year 2015
echo date("M-d-Y", easter_date($year));     
?>
```

时 Easter_Days()函数的工作原理

帖子主题：Re：Колибри

**程序 3：**下面的程序解释了同时传递两个参数时 Easter_Days()函数的工作原理。

```
<?php
// PHP program to demonstrate the 
// easter_days() function 
// when both parameters are passed 

$year = 2014; 

// no of days for Easter after march 21 of year 2014 
// of Gregorian Calendar
echo easter_days($year, CAL_EASTER_ROMAN), "\n";  
?>
```

帖子主题：Re：Колибри

**引用：**[http://php.net/manual/en/function.easter-days.php](http://php.net/manual/en/function.easter-days.php)