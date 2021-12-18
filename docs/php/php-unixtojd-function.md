# PHP|unixtojd()函数

> Original: [https://www.geeksforgeeks.org/php-unixtojd-function/](https://www.geeksforgeeks.org/php-unixtojd-function/)

Unixtojd()是 PHP 中的一个内置函数，用于将 Unix 时间戳转换为儒略日计数。 UNIX 时间戳是一种以秒为单位跟踪时间的方法。 这个计数从 Unix 纪元 1970 年 1 月 1 日 UTC 开始。 因此，UNIX 时间戳仅仅是特定日期和 Unix 纪元之间的秒数。

**语法：**

```php
unixtojd( $unix )
```

**参数：**该函数接受如上所示的单个参数，该参数是可选的。 **$unix**指定转换为儒略日计数的 Unix 时间戳。

**返回值：**此函数返回作为转换为 Julian day Integer 的参数传递的 Unix 时间戳。 如果没有传递任何参数，则返回当前的儒略日整数。 我们可以使用[jdtogregorian()](https://www.geeksforgeeks.org/php-jdtogregorian-function/)函数将儒略日整数转换为格里高利日期，以知道确切的日期。

例如：

```php
Input : $unix = 1524909427
Output : 2458237
Explanation: The Gregorian date is 4/28/2018 of 
the given unix timestamp 

Input : $unix = 5677896
Output : 2440653
Explanation: The Gregorian date is 3/7/1970 of 
the given unix timestamp 
```

**注意：**此函数只能取儒略日整数，直到公历日期**1/19/2038**，因为在此日期 Unix 时间戳将因 32 位溢出而停止工作。

下面的程序演示了 unixtojd()函数。

**程序 1：**下面的程序演示了未传递参数时函数的使用。

## PHP

```php
<?php
// PHP program to demonstrate the use of unixtojd()
// function when no parameter is passed

// takes the current date as unix timestamp
$jd = unixtojd();

// prints the julian Day integer
echo "The Julian Day integer is ", ($jd), "\n";

// prints the corresponding Gregorian date
echo "The Gregorian date is ", jdtogregorian($jd);
?>
```

产出：

```php
The Julian Day integer is 2458237
The Gregorian date is 4/28/2018
```

**程序 2：**下面的程序演示了传递参数时函数的用法。

## PHP

```php
<?php
// PHP program to demonstrate the use of unixtojd()
// function when parameter is passed

// takes a unix timestamp in parameter
$jd = unixtojd(5677896);

// prints the julian Day integer
echo "The Julian Day integer is ", ($jd), "\n";

// prints the corresponding Gregorian date
echo "The Gregorian date is ", jdtogregorian($jd);
?>
```

产出：

```php
The Julian Day integer is 2440653
The Gregorian date is 3/7/1970
```

**引用：**[http://php.net/manual/en/function.unixtojd.php](http://php.net/manual/en/function.unixtojd.php)