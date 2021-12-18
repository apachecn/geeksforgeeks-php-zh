# PHP|gmp_Powm()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_powm-function/](https://www.geeksforgeeks.org/php-gmp_powm-function/)

Gmp_powerm()是 PHP 中的一个内置函数，用于计算两个 GMP 数的幂与另一个 GMP 数的模数。([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：用于大数)

**语法：**

```php
gmp_pow( $base, $exp, $mod)
```

**参数：**函数接受三个必选参数$base、$exp 和$mod

1.  **$BASE**-它是基数。
2.  **$exp**-它是提升到基础的力量。
3.  **$mod**-它返回与*$mod*相除后的余数

**注意：**在 PHP 5.6 版和更高版本中，所有参数都是 GMP 对象，或者我们也可以传递数字字符串，前提是可以将该字符串转换为数字。

**返回值：**此函数返回一个正的[gmp](http://php.net/manual/en/class.gmp.php)数字，等于**(base<sup>exp</sup>)%mod**

例如：

```php
Input : $base = "2" $exp = "2" $mod = 3
Output : 1

Input : $base = "4" $exp = "2" $mod = 10
Output : 6

```

以下程序说明了 gmp_powerm()函数：

**程序 1：**下面的程序演示了当 GMP 编号作为参数传递时，gmp_powerm()函数的工作原理。

```php
<?php
// PHP program to calculate power raised 
// to a number mdoulo mod

// GMP number as arguments 
$base = gmp_init("100", 2);
$exp = gmp_init("10", 2); 
$mod = gmp_init("1010", 2);

// function calculates the pow raised to 
// number modulo mod 
$powm = gmp_powm($base, $exp, $mod);  // 4^2%10 

// gmp_strval converts GMP number to string 
// representation in given base(default 10).
echo gmp_strval($powm, 2);
?>
```

产出：

```php
110
```

**程序 2：**下面的程序演示了将数字字符串作为参数传递时 gmp_powerm()的工作方式。

```php
<?php
// PHP program to calculate power raised 
// to a number modulo m

// numeric strings as arguments
$base = "4";
$exp = "2"; 
$mod = "10";

// function calculates the pow raised to 
// number  4^2%10
$powm = gmp_powm($base, $exp, $mod);

echo $powm;
?>
```

产出：

```php
6
```

**引用：**
[http://php.net/manual/en/function.gmp-powm.php](http://php.net/manual/en/function.gmp-powm.php)