# PHP|Easter_Date()函数

> Original: [https://www.geeksforgeeks.org/php-easter_date-function/](https://www.geeksforgeeks.org/php-easter_date-function/)

**Easter_Date()**函数是 PHP 中的一个内置函数，它返回作为参数传递的年份中的复活节日期。 如果未将任何参数作为参数传递，则将当前年份视为默认年份。

**语法：**

```php
easter_date( $year )
```

**参数：**该函数接受一个可选参数*$Year*，该参数指定要返回其复活节日期的年份。 年份只能是 1970 年到 2037 年之间的数字。 当年份超出范围时，它会返回一条错误消息。

**返回值：**它返回参数中传递的给定年份的复活节日期。 如果没有传递任何参数，则返回当年的复活节日期。

例如：

```php
Input : 2018
Output : Apr-01-2018

Input : 2017
Output : Apr-16-2017

```

以下程序说明了 Easter_Date()函数：

**程序 1：**程序演示未传递参数时的函数。

```php
<?php
// PHP program to demonstrate the
// working of easter_date() function 
// when no parameter is passed 

// prints the date of Easter of year 2018
// when no parameter is passed 
echo date("M-d-Y", easter_date()), "\n";   

// current year to verify 
$year = 2018; 
echo date("M-d-Y", easter_date($year));   
?>
```

产出：

```php
Apr-01-2018
Apr-01-2018
```

**程序 2：**程序演示参数传递时的功能。

```php
<?php
// PHP program to demonstrate the
// working of easter_date() function 
// when parameter is passed 

$year = 2017; 
echo date("M-d-Y", easter_date($year)), "\n"; 

$year = 2010; 
echo date("M-d-Y", easter_date($year)), "\n"; 

$year = 2000; 
echo date("M-d-Y", easter_date($year)); 
?>
```

产出：

```php
Apr-16-2017
Apr-04-2010
Apr-23-2000
```

**程序 3：**程序演示参数传递超出范围时的功能。

```php
<?php
// PHP program to demonstrate the
// working of easter_date() function 
// when parameter is out of range

$year = 2050; 

echo date("M-d-Y", easter_date($year)), "\n"; 

?>
```

产出：

```php
PHP Warning:  easter_date(): This function is only valid 
for years between 1970 and 2037 inclusive in
/home/df540ecbab7094243e7668326260e785.php on line 8

```

**引用：**
[http://php.net/manual/en/function.easter-date.php](http://php.net/manual/en/function.easter-date.php)