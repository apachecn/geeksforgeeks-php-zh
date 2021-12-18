# PHP|gmp_abs()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_abs-function/](https://www.geeksforgeeks.org/php-gmp_abs-function/)

Gmp_abs()是 PHP 中的一个内置函数，用于计算 GMP 数字的绝对值([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：用于大数)。

**语法：**

```
gmp_abs( $num )
```

**参数：**此函数接受 GMP 编号作为参数，如上面的语法所示。 它可以是 PHP 5.6 版和更高版本中的 GMP 对象，也可以是一个数字字符串，前提是可以将后者转换为数字。此函数计算该数字的绝对值并返回该值。

**返回值：**此函数返回一个正 GMP 数，它是作为参数传递的数的绝对值。

例如：

```
Input : "16497863358"
Output : 16497863358

Input : "-16497863358"
Output : 16497863358

```

以下程序说明了 gmp_abs()函数在 PHP 中的使用：

**程序 1：**

```
<?php

// Passing a positive number
// as a numeric string
$val1 = gmp_abs("16497863358");

// Passing a negative number
// as a numeric string
$val2 = gmp_abs("-16497863358");

echo gmp_strval($val1);
echo "\n";
echo gmp_strval($val2);

?>
```

产出：

```
16497863358
16497863358

```

**程序 2：**

```
<?php

// Passing a positive number
// as a numeric string
$val1 = gmp_abs("1897023411");

// Passing a negative number
// as a numeric string
$val2 = gmp_abs("-1897023411");

echo gmp_strval($val1);
echo "\n";
echo gmp_strval($val2);

?>
```

发帖主题：Re：Колибри0.7.8.0

```
1897023411
1897023411

```

**引用：**
[http://php.net/manual/en/function.gmp-abs.php](http://php.net/manual/en/function.gmp-abs.php)