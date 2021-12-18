# PHP|gmp_root()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_root-function/](https://www.geeksforgeeks.org/php-gmp_root-function/)

GMP_ROOT()是 PHP 中的一个内置函数，它返回 GMP 数的 N 次方根的整数部分([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：表示大数)。
**语法：**

```php
gmp_root( $num, $n )

```

**参数：**该函数接受两个必选参数$num 和$n。

1.  **$num**-这是返回其第 n 次根的整数部分的 GMP 编号。 在 PHP 5.6 版和更高版本中，该参数是一个 GMP 对象，或者我们也可以传递一个数字字符串，前提是可以将该字符串转换为数字。
2.  **$n**-数字的正 n 次根。 它是一个整数值。

**返回值：**此函数返回一个正的[gmp](http://php.net/manual/en/class.gmp.php)数，它是$num 的 N 次方根的整数部分。*
示例：{

```php
Input : $num = "20" $n = 2
Output : 4 

Input : $num = "9" $n = 2
Output : 2

```

下面的程序说明了 gmp_root()函数：
**程序 1：**下面的程序演示了将 gmp 编号作为参数传递时 gmp_root()函数的工作方式。

## PHP

```php
<?php
// PHP program to calculate the
// integer part of N-th root of 
// a GMP number

// GMP number as arguments
$num = gmp_init("1001", 2);
$n = 3;

// function calculates the pow raised to
// number modulo mod 

//  integer part of cubic root of 9
$root = gmp_root($num, $n); 

// gmp_strval Convert GMP number to string
// representation in given base(default 10).
echo gmp_strval($root, 2);
?>
```