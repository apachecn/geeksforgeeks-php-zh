# PHP|模逆

的 gmp_invert()

> Original: [https://www.geeksforgeeks.org/php-gmp_invert-inverse-modulo/](https://www.geeksforgeeks.org/php-gmp_invert-inverse-modulo/)

Gmp_invert()是 PHP 中的一个内置函数，用于在另一个 GMP 编号下查找 GMP 编号的模逆([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：对于大数)。

模逆是一个数字 x，使得：

```php
a x ≡ 1 (mod b) 

```

X 的值应为{0，1，2，…。 B-1}，即在模 b 整数环中。

**语法：**

```php
gmp_invert ( $a, $b )
```

**参数：**此函数接受两个 GMP 编号*$a*和*$b*，如上面的语法所示。 此函数在模*$b*下查找*$a*的逆。 这些参数可以是 PHP 5.6 版和更高版本中的 GMP 对象，也可以传递数字字符串，前提是可以将该字符串转换为数字。

**返回值：**此函数返回一个 GMP 数，它是作为参数传递给它的两个数的计算反模数。 如果找不到给定两个数的逆模，则此函数返回 FALSE。

例如：

```php
Input:  $a = 3, $b = 11
Output: 4
Since (4*3) mod 11 = 1, 4 is modulo inverse of 3
One might think, 15 also as a valid output as "(15*3) mod 11" 
is also 1, but 15 is not in ring {0, 1, 2, ... 10}, so not 
valid.

Input:  $a = 10, $b = 17
Output: 12
Since (10*12) mod 17 = 1, 12 is modulo inverse of 3

```

以下程序说明了 PHP 中的 gmp_invert()函数：

**程序 1：**当作为 GMP 编号的数字字符串作为参数传递时，计算逆模的程序。

```php
<?php
// PHP program to calculate inverse modulo

// strings as GMP numbers 
$a = "3";
$b = "11";

// calculates the inverse modulo of a number
$invMod = gmp_invert($a, $b);
echo $invMod."\n";

// calculates the inverse modulo of a number
$a = "10"; $b = "17";
$invMod = gmp_invert($a, $b);
echo $invMod."\n";

?>
```

产出：

```php
4
12

```

**程序 2：**当 GMP 编号作为参数传递时计算逆模的程序。

```php
<?php
// PHP program to calculate inverse modulo

// creating GMP numbers using gmp_init() 
$a = gmp_init(3, 10);
$b = gmp_init(11, 10);

// calculates the inverse modulo of a number
$invMod = gmp_invert($a, $b);
echo $invMod."\n";

// calculates the inverse modulo of a number
$a = gmp_init(10, 10); 
$b = gmp_init(17, 10);
$invMod = gmp_invert($a, $b);
echo $invMod."\n";

?>
```

产出：

```php
4
12

```

**引用：**
[http://php.net/manual/en/function.gmp-invert.php](http://php.net/manual/en/function.gmp-invert.php)