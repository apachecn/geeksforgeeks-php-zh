# PHP|gmp_testbit()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_testbit-function/](https://www.geeksforgeeks.org/php-gmp_testbit-function/)

Gmp_testbit()是 PHP 中的一个内置函数，用于检查是否设置了给定 GMP 编号的指定位([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：对于大数)。

**语法：**

```php
gmp_testbit($num, $index)
```

**参数：**此函数接受两个必需的参数，如下所述：

1.  **$num-** this function accepts a GMP number *$num* to check its location. This parameter can be a GMP object in PHP version 5.6 and later, or you can pass a numeric string, provided that the string can be converted to a number.
2.  **$index-** to check the specified index of the bits in its $num. It is an integer.

**返回值：**如果设置了指定的**$index**位，则函数返回**true**，否则返回**false**。

例如：

```php
Input : $num=4 $index=2
Output :  true

Input : $num=9 $index=2
Output :  false

```

以下程序说明了 gmp_testbit()函数的用法：

**程序 1：**下面的程序演示了当 GMP 编号作为参数传递时，gmp_testbit()函数的工作原理。

```php
<?php
// PHP program to check the sign 
// of a number 

// numeric string arguments 
$num = gmp_init("1001", 2);
$index1 = 2; 
$index2 = 0; 

// checks if the 2nd index bit in 9 (1001) is set or not
var_dump(gmp_testbit($num, $index1))."\n";  

// checks if the 0th index bit in 9 (1001) is set or not
var_dump(gmp_testbit($num, $index2));  
?>
```

帖子主题：Re：Колибри

**程序 2：**下面的程序演示了将数字字符串作为参数传递时 gmp_testbit()的工作方式。

```php
<?php
// PHP program to check the sign 
// of a number 

// numeric string arguments 
$num = "9";
$index1 = 2; 
$index2 = 3; 

// checks if the 2nd index bit in 9 (1001) 
// is set or not
var_dump(gmp_testbit($num, $index1))."\n";  

// checks if the 3rd index bit in 9 (1001) 
// is set or not
var_dump(gmp_testbit($num, $index2));  
?>
```

帖子主题：Re：Колибри

**引用：**[http://php.net/manual/en/function.gmp-testbit.php](http://php.net/manual/en/function.gmp-testbit.php)