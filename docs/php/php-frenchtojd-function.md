# PHP|frenchtojd()函数

> Original: [https://www.geeksforgeeks.org/php-frenchtojd-function/](https://www.geeksforgeeks.org/php-frenchtojd-function/)

Frenchtojd()函数是一个内置函数，用于将[法国日期](https://en.wikipedia.org/wiki/French_Republican_Calendar#Months)转换为[儒略日计数](https://en.wikipedia.org/wiki/Julian_calendar)。 该函数接受格式为*$Month/$day/$Year*的三个参数，表示法国共和历中的日期，并将其转换为儒略日计数。

**语法：**

```
frenchtojd( $month, $day, $year) 
```

**参数：**此函数接受三个必选参数，如上所示，如下所述：

1.  **$Month-**此参数指定法国日历中的月份编号。 月份数字在 1-13(含 1-13)的范围内。 如果传递的月份数字大于 12 或小于 0，则儒略日返回为 0。
2.  **$day-**此参数指定法国日历中的日期。 天数在 1-30 之间(含 1-30 天)。 如果传递的天数大于 31 或小于 0，则儒略日返回为 0。 闰年不在考虑之列。
3.  **$Year-**此参数指定法国日历中的年份。 年份编号的范围为 1-14(含 1-14)。 如果通过的年份数大于 14 或小于 1，则儒略日返回为 0。 闰年不在考虑之列。

**返回值：**此函数返回转换为儒略日计数的法国日期。

例如：

```
Input : $month=3, $day=11, $year=12
Output : 2379928 

Input : $month=4, $day=8, $year=13
Output : 2380320

```

下面的程序演示了 frenchtojd()函数。

**程序 1：**下面的程序演示了 frenchtojd()函数的用法。

```
<?php
// PHP program to demonstrate the
// use of frenchtojd() function 

// converts date to julian integer 
$jd=frenchtojd(4, 8, 13);

// prints the julian day integer
echo ($jd);
?>
```

产出：

```
 2380320
```

**程序 2：**下面的程序演示了日和月超出范围时的情况。

```
<?php
// PHP program to demonstrate the
// use of frenchtojd() function 

// converts date to julian integer 
// month is out of range
$jd=frenchtojd(22, 8, 11);

// prints the julian day integer
echo ($jd), "\n"; 

// day is out of range
$jd=frenchtojd(4, 32, 11);
echo ($jd); 
?>
```

产出：

```
0
0
```

**引用：**
[http://php.net/manual/en/function.frenchtojd.php](http://php.net/manual/en/function.frenchtojd.php)