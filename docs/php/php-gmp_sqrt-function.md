# PHP|gmp_sqrt()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_sqrt-function/](https://www.geeksforgeeks.org/php-gmp_sqrt-function/)

Gmp_sqrt()是 PHP 中的一个内置函数，用于计算 GMP 数字的平方根([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：用于大数)。 此函数仅返回 GMP 编号平方根的整数部分。

**语法：**

```
gmp_sqrt ( $num )
```

**参数：**此函数接受 GMP 编号*$num*作为强制参数，如上面的语法所示。 在 PHP 5.6 版和更高版本中，该参数可以是 GMP 对象，也可以传递数字字符串，前提是可以将该字符串转换为数字。

**返回值：**此函数返回一个 GMP 编号，它是作为参数传递给它的 GMP 编号的平方根。 此函数仅返回作为参数传递给它的 GMP 编号的平方根的整数部分。

例如：

```
Input : "9"
Output : 3

Input : "24"
Output : 4

```

以下程序说明了 PHP 中的 gmp_sqrt()函数：

**程序 1：**当作为 GMP 编号的数字字符串作为参数传递时，计算 GMP 编号的平方根的程序。

```
<?php
// PHP program to calculate the square root 
// of a GMP number passed as arguments 

// strings as GMP numbers 
$num1 = "9";
$num2 = "24";

// calculates the square root of a GMP number
$squareRoot = gmp_sqrt($num1);
echo $squareRoot."\n";

// calculates the square root of a GMP number
$squareRoot = gmp_sqrt($num2);
echo $squareRoot."\n";

?>
```

产出：

```
3
4

```

**程序 2：**当 GMP 编号作为参数传递时，计算 GMP 编号的平方根的程序。

```
<?php
// PHP program to calculate the square root 
// of a GMP number

// creating GMP numbers using gmp_init()
$num1 = gmp_init(9, 10);
$num2 = gmp_init(24, 10);

// calculates the square root of a GMP number
$squareRoot = gmp_sqrt($num1);
echo $squareRoot."\n";

// calculates the square root of a GMP number
$squareRoot = gmp_sqrt($num2);
echo $squareRoot."\n";

?>
```

产出：

```
3
4

```

**引用：**
[http://php.net/manual/en/function.gmp-sqrt.php](http://php.net/manual/en/function.gmp-sqrt.php)