# PHP|jdtofrch()函数

> Original: [https://www.geeksforgeeks.org/php-jdtofrench-function/](https://www.geeksforgeeks.org/php-jdtofrench-function/)

函数的作用是：将[儒略日整数](https://en.wikipedia.org/wiki/Julian_calendar)转换为[法国日期。](https://en.wikipedia.org/wiki/French_Republican_Calendar) 此函数接受儒略日整数，并以*$月/$日/$年返回转换后的法国日期。*

**语法：**

```
jdtofrench($jd)
```

**参数：**该函数接受一个指定儒略日的强制参数*$jd*。

**返回值：**此函数返回法国日期。 日期的返回格式为*$月/$日/$年。* 如果儒略日整数作为 0 传递，则返回 0/0/0 作为输出。

例如：

```
Input : 2379254
Output : 5/8/10 

Input : 2380229
Output : 1/7/13

```

下面的程序说明了 jdtofrch()函数。

**程序 1：**下面的程序说明了 jdtofrch()函数的用法。

```
<?php
// PHP program to demonstrate the
// use of jdtofrench() function 

// converts date to julian integer 
$jd = frenchtojd(1, 7, 13);

// prints the julian day integer 
echo "The julian day integer is ", $jd, "\n";

// converts the Julian day to French date
$date = jdtofrench($jd);

// prints the date
echo "The french date initially taken was ", ($date), "\n"; 

?>
```

产出：

```
The julian day integer is 2380229
The french date initially taken was 1/7/13

```

**程序 2：**下面的程序显示了传递无效儒略日整数时的输出。

```
<?php
// PHP program to demonstrate the
// use of jdtofrench() function  
// in case of out of range parameter is passed 

// converts date to julian integer 
$jd = frenchtojd(1, 7, 18);

// prints the julian day integer as 0 as year is out of range
echo "The julian day integer is ", $jd, "\n";

// converts the Julian day to French date
$date = jdtofrench($jd);

// prints the date as 0/0/0 as french year is out of range
echo "The french date initially taken was ", ($date), "\n"; 

?>
```

产出：

```
The julian day integer is 0
The french date initially taken was 0/0/0

```

**引用：**
[http://php.net/manual/en/function.jdtofrench.php](http://php.net/manual/en/function.jdtofrench.php)