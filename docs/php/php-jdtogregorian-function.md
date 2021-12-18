# PHP|jdtogregorian()函数

> Original: [https://www.geeksforgeeks.org/php-jdtogregorian-function/](https://www.geeksforgeeks.org/php-jdtogregorian-function/)

Jdtogregorian()函数是一个内置函数，用于将[儒略日整数](https://en.wikipedia.org/wiki/Julian_calendar)转换为[公历日期](https://en.wikipedia.org/wiki/Gregorian_calendar)。 该函数接受儒略日整数，并以*$月/$日/$年返回转换后的公历日期。*

**语法：**

```php
jdtogregorian($jd)
```

**参数：**该函数接受一个指定儒略日的强制参数*$jd*。

**返回值：**此函数返回公历日期。 日期的返回格式为*$月/$日/$年。*

例如：

```php
Input : 2458209
Output : 3/31/2018

Input : 2458236
Output : 4/27/2018

```

下面的程序说明了 jdtogregorian()函数。

**程序 1：**下面的程序说明了 jdtogregorian()函数的用法。

```php
<?php
// PHP program to demonstrate the
// use of jdtogregorian() function 

// converts date to julian integer 
$jd = gregoriantojd(3, 31, 2018);

// converts the Julian day to Gregorian date
$date = jdtogregorian($jd);

// prints the date
echo ($date), "\n"; 

?>
```

产出：

```php
3/31/2018
```

**程序 2：**下面的程序显示了传递无效儒略日整数时的输出。

```php
<?php
// PHP program to demonstrate the output
// of jdtogregorian() function when 0 is 
// passed as Julian Day, which is invalid

// converts the Julian day to Gregorian date 
// invalid hence outputs 0/0/0 
$date = jdtogregorian(0);

// prints the date
echo ($date), "\n"; 

?>
```

产出：

```php
0/0/0
```

**引用：**
[http://php.net/manual/en/function.jdtogregorian.php](http://php.net/manual/en/function.jdtogregorian.php)