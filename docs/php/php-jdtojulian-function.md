# PHP|jdtojulian()函数

> Original: [https://www.geeksforgeeks.org/php-jdtojulian-function/](https://www.geeksforgeeks.org/php-jdtojulian-function/)

Jdtojulian()函数是 PHP 中的一个内置函数，用于将儒略日计数转换为儒略历日期。 它将儒略日计数转换为包含*月/日/年*格式的儒略历日期的字符串。
**语法：**和

```
int jdtojulian( $julianday )
```

**参数：**此函数接受单个参数*$julianday*，这是必需的。 它包含以整数形式表示的朱利安日期。
**返回值：**此函数以*月/日/年*格式的字符串形式返回儒略日期。
以下程序说明 PHP 中的 jdtojulian()函数。
**程序 1：**和

## PHP

```
<?php

// Converts a Julian calendar date 
// to Julian Day count.
$jdate = juliantojd(10, 25, 1996);

// Print the Julian Day count.
echo "JulianToJD is : ".$jdate . "\n";

// First converts the julian day to Julian 
// Calendar date and then print it.
echo "JDToJulian is : ".jdtojulian($jdate);

?>
```

**Output:** 

```
JulianToJD is : 2450395
JDToJulian is : 10/25/1996
```

**程序 2：**和

## PHP

```
<?php

// Converts Julian calendar Date 
// to Julian Day count.
$jdate = juliantojd(1, 10, 1998);

// Print the Julian Day count
echo "Julian Day Count : ".$jdate . "\n";

// Converts Julian Day count to
// the Julian calendar Date
$julian = jdtojulian($jdate);

// Print the julian calendar Date.
echo "Julian Calendar Date : ".$julian;

?> 
```

**Output:** 

```
Julian Day Count : 2450837
Julian Calendar Date : 1/10/1998
```

**相关文章：**和

*   [PHP|cal_day_in_Month()函数](https://www.geeksforgeeks.org/php-cal_days_in_month-function/)
*   [PHP|Easter_Days()函数](https://www.geeksforgeeks.org/php-easter_days-function/)

**引用：**[http://php.net/manual/en/function.jdtojulian.php](http://php.net/manual/en/function.jdtojulian.php)