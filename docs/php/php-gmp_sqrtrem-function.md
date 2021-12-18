# PHP|gmp_sqrtrem()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_sqrtrem-function/](https://www.geeksforgeeks.org/php-gmp_sqrtrem-function/)

Gmp_sqrtrem()是 PHP 中的一个内置函数，用于计算 GMP 数([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：对于大数)的平方根和余数。 此函数还作为 gmp_sqrt()函数仅返回 GMP 编号平方根中的整数部分。 余数基本上是 GMP 数字与此函数返回的平方根值之间的差值。

**语法：**

```
gmp_sqrtrem ( $num )
```

**参数：**此函数接受 GMP 编号*$num*作为强制参数，如上面的语法所示，我们要计算其平方根。 在 PHP 5.6 版和更高版本中，该参数可以是 GMP 对象，也可以传递数字字符串，前提是可以将该字符串转换为数字。

**返回值：**此函数返回两个 GMP 编号的数组。 该数组中的第一个元素是作为参数传递给函数的 GMP 编号的平方根的整数部分，第二个元素是余数。 余数计算为 GMP 编号与该数组第一个元素的平方之间的差值。

例如：

```
Input : "9"
Output : 3

Input : "24"
Output : 4

```

以下程序说明了 PHP 中的 gmp_sqrtrem()函数：

**程序 1：**当作为 GMP 编号的数字字符串作为参数传递时，用 GMP 编号的余数计算平方根的程序。

```
<?php
// PHP program to calculate the square root 
// of a GMP number

// passing numeric strings as GMP numbers
$num = gmp_init("24");

// calculates the square root of a GMP number
// with remainder
list($squareRoot, $rem) = gmp_sqrtrem($num);

echo $squareRoot." ".$rem;

?>
```

产出：

```
4 8

```

**程序 2：**当 GMP 编号作为参数传递时，用 GMP 编号的余数计算平方根的程序。

```
<?php
// PHP program to calculate the square root 
// of a GMP number

// creating GMP numbers using gmp_init()
$num = gmp_init(24, 10);

// calculates the square root of a GMP number
// with remainder
list($squareRoot, $rem) = gmp_sqrtrem($num);

echo $squareRoot." ".$rem;

?>
```

产出：

```
4 8

```

**引用：**
[http://php.net/manual/en/function.gmp-sqrtrem.php](http://php.net/manual/en/function.gmp-sqrtrem.php)