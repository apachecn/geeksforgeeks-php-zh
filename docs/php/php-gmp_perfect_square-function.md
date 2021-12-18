# PHP|gmp_Perfect_Square()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_perfect_square-function/](https://www.geeksforgeeks.org/php-gmp_perfect_square-function/)

Gmp_Perfect_Square()是 PHP 中的一个内置函数，用于检查给定的 GMP 数字([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：对于大数)是否为完美平方。

**语法：**

```php
gmp_perfect_square($num)
```

**参数：**该函数接受一个 GMP 编号*$num*。 在 PHP 5.6 版和更高版本中，该参数可以是 GMP 对象，也可以传递数字字符串，前提是可以将该字符串转换为数字。

**返回值：**如果给定的数字*$num*是完美平方，则函数返回**true**，否则返回*false*。

例如：

```php
Input : $num=25 
Output :  true

Input : $num=10
Output :  false

```

以下程序说明了 gmp_Perfect_Square()函数的用法：

**程序 1：**下面的程序演示了当 GMP 编号作为参数传递时，gmp_Perfect_Square()函数的工作原理。

```php
<?php
// PHP program to check the if the 
// number is perfect square or not

// numeric string arguments 
$num = gmp_init("1001", 2);
// checks if 9 (1001) is a perfect number or not
var_dump(gmp_perfect_square($num))."\n";  

$num = gmp_init("11001", 2);
// checks if 25 (11001) is a perfect number or not
var_dump(gmp_perfect_square($num))."\n";   

$num = gmp_init("1100", 2);
// checks if 12 (1100) is a perfect number or not
var_dump(gmp_perfect_square($num));  
?>
```

产出：

```php
bool(true) 
bool(true)
bool(false)
```

**程序 2：**下面的程序演示了将数字字符串作为参数传递时 gmp_Perfect_Square()的工作原理。

```php
<?php
// PHP program to check the if the 
// number is perfect square or not

// numeric string arguments 
$num = "9";
// checks if 9 (1001) is a perfect number or not
var_dump(gmp_perfect_square($num))."\n";  

$num = "25";
// checks if 25 (11001) is a perfect number or not
var_dump(gmp_perfect_square($num))."\n";   

$num = "12";
// checks if 12 (1100) is a perfect number or not
var_dump(gmp_perfect_square($num));  
?>
```

产出：

```php
bool(true) 
bool(true)
bool(false)
```

**引用：**
[http://php.net/manual/en/function.gmp-perfect-square.php](http://php.net/manual/en/function.gmp-perfect-square.php)