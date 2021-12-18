# PHP|gmp_power()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_pow-function/](https://www.geeksforgeeks.org/php-gmp_pow-function/)

GMP_POW()是 PHP 中的一个内置函数，用于计算 GMP 数字和整数的幂([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：表示大数)。

**语法：**

```
gmp_pow( $base, $exp )
```

**参数：**该函数接受两个必选参数$base 和$exp。

1.  $BASE-它是基数。 在 PHP 5.6 版和更高版本中，该参数可以是 GMP 对象，也可以传递数字字符串，前提是可以将该字符串转换为数字。
2.  $exp-它是提升到基础的力量

**返回值：**此函数返回一个正的 GMP 数字，相当于$BASE<sup>$EXP</sup>
示例：

```
Input : $base = "2" $exp = 2
Output : 4

Input : $base = "0" $exp = 0
Output : 1 

```

以下程序说明了 gmp_power()函数：

**程序 1：**下面的程序演示了当 GMP 编号作为参数传递时，gmp_power()函数的工作原理。

```
<?php
// PHP program to calculate power raised 
// to a number 

// GMP number as argument 
$base = gmp_init("100", 2);
$exp = 2; 

// function calculates the pow raised to 
// number  
$pow = gmp_pow($base, $exp);  // 4^2 

// gmp_strval Convert GMP number to string 
// representation in given base(default 10).
echo gmp_strval($pow, 2) . "\n";
?>
```

产出：

```
10000
```

**程序 2：**下面的程序演示了将数字字符串作为参数传递时 gmp_power()的工作方式。

```
<?php
// PHP program to calculate power raised 
// to a number 

// numeric string as argument
$base = "4";
$exp = 2; 

// function calculates the pow raised to 
// number  4^2 
$pow = gmp_pow($base, $exp);

echo $pow;
?>
```

产出：

```
10000
```

**引用：**
[http://php.net/manual/en/function.gmp-pow.php](http://php.net/manual/en/function.gmp-pow.php)