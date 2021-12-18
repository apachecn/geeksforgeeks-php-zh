# PHP|gmp_popcount()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_popcount-function/](https://www.geeksforgeeks.org/php-gmp_popcount-function/)

Gmp_popcount()是 PHP 中的一个内置函数，用于查找 GMP 编号的人口计数([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：用于大数)。 我们也可以说，此函数用于查找 GMP 编号的二进制表示中的设置位数。

**语法：**

```
gmp_popcount ( $num )
```

**参数：**此函数接受 GMP 编号*$num*作为强制参数，如上面的语法所示。 在 PHP 5.6 版和更高版本中，该参数可以是 GMP 对象，也可以传递数字字符串，前提是可以将该字符串转换为数字。

**返回值：**此函数返回一个整数，它是作为参数传递给它的 GMP 编号的总体计数或二进制表示的设置位数。

例如：

```
Input : "9"
Output : 2

Input : "25"
Output : 3

```

以下程序说明了 PHP 中的 gmp_popcount()函数：

**程序 1：**当作为 GMP 编号的数字字符串作为参数传递时，计算数字的总体计数的程序。

```
<?php
// PHP program to calculate population count 
// of a GMP number passed as arguments 

// strings as GMP numbers 
$num1 = "9";
$num2 = "25";

// calculates the population count of a number
$pcount = gmp_popcount($num1);
echo $pcount."\n";

// calculates the population count of a number
$pcount = gmp_popcount($num2);
echo $pcount."\n";

?>
```

产出：

```
2
3

```

**程序 2：**当 GMP 编号作为参数传递时，计算一个数字的总体计数的程序。

```
<?php
// PHP program to calculate population count 
// of a GMP number passed as arguments 

// creating GMP numbers using gmp_init()
$num1 = gmp_init(9, 10);
$num2 = gmp_init(25, 10);

// calculates the population count of a number
$pcount = gmp_popcount($num1);
echo $pcount."\n";

// calculates the population count of a number
$pcount = gmp_popcount($num2);
echo $pcount."\n";

?>
```

产出：

```
2
3

```

**引用：**
[http://php.net/manual/en/function.gmp-popcount.php](http://php.net/manual/en/function.gmp-popcount.php)