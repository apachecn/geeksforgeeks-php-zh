# PHP|gmp_hamdist()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_hamdist-function/](https://www.geeksforgeeks.org/php-gmp_hamdist-function/)

Gmp_hamdist()是 PHP 中的一个内置函数，用于查找两个 GMP 数字之间的汉明距离([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：用于大数)。

[两个数之间的汉明距离](https://en.wikipedia.org/wiki/Hamming_distance)被定义为它们的二进制表示中不匹配的位数。

**语法：**

```php
gmp_hamdist ( $num1, $num2)
```

**参数：**此函数接受两个 GMP 编号*$num1*和*$num2*，如上面的语法所示。 这两个参数都是必须传递的，并且必须为正数。 此函数用于查找两个数字$num1 和$num2 之间的汉明距离。 这些参数可以是 PHP 5.6 版和更高版本中的 GMP 对象，也可以传递数字字符串，前提是可以将该字符串转换为数字。

**返回值：**此函数返回一个 GMP 数，它是作为参数传递给它的两个数的计算汉明距离。

例如：

```php
Input:  $a = "3", $b = "11"
Output: 1
Explanation: Binary representation of 3 is 0011
Binary representation of 11 is 1011\. So, they 
differ by only 1 bit.

Input:  $a = "4", $b = "4"
Output: 0

```

以下程序说明了 PHP 中的 gmp_hamdist()函数：

**程序 1：**当作为 GMP 编号的数字串作为参数传递时，计算汉明距离的程序。

```php
<?php
// PHP program to calculate hamming distance

// strings as GMP numbers 
$a = "3";
$b = "11";

// calculates the hamming distance
$hamDist = gmp_hamdist($a, $b);
echo $hamDist."\n";

// calculates the hamming distance
$a = "4"; $b = "4";
$hamDist = gmp_hamdist($a, $b);
echo $hamDist."\n";

?>
```

产出：

```php
4
12

```

**程序 2：**当 GMP 编号作为参数传递时计算汉明距离的程序。

```php
<?php
// PHP program to calculate hamming distance

// creating GMP numbers using gmp_init() 
$a = gmp_init("11", 2); // 3 in decimal
$b = gmp_init("1011", 2); // 11 in decimal

// calculates the hamming distance
$hamDist = gmp_hamdist($a, $b);
echo $hamDist."\n";

// calculates the hamming distance
$a = gmp_init("100", 2);
$b = gmp_init("100", 2);
$hamDist = gmp_hamdist($a, $b);
echo $hamDist."\n";

?>
```

产出：

```php
1
0

```

**引用：**
[http://php.net/manual/en/function.gmp-hamdist.php](http://php.net/manual/en/function.gmp-hamdist.php)