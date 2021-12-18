# PHP|gmp_nextPrime()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_nextprime-function/](https://www.geeksforgeeks.org/php-gmp_nextprime-function/)

Gmp_nextPrime()是 PHP 中的一个内置函数，用于计算略大于给定 GMP 数的质数([GNU Multiple Precision：for Large Numbers](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library))。

**语法：**

```
gmp_nextprime($num)
```

**参数：**此函数接受 GMP 编号*$num*作为强制参数，如上面的语法所示，我们要查找其下一个素数。 在 PHP 5.6 版和更高版本中，该参数可以是 GMP 对象，也可以传递数字字符串，前提是可以将该字符串转换为数字。

**返回值：**此函数返回一个 GMP 号，它是刚刚大于作为参数传递给它的 GMP 号的质数。

例如：

```
Input : gmp_nextprime("15")
Output : 17

Input : gmp_nextprime("21")
Output : 23

```

以下程序说明了 PHP 中的 gmp_nextPrime()函数：

**程序 1：**当将数字字符串作为 GMP 编号作为参数传递时，计算刚好大于 GMP 编号的质数的程序。

```
<?php
// PHP program to calculate the prime number greater 
// than that of a GMP number passed as arguments 

// strings as GMP numbers 
$num = "135";

// gives the prime number just greater
// than 135 as a GMP number
$res = gmp_nextprime($num);

echo $res;

?>
```

产出：

```
137

```

**程序 2：**当 GMP 编号作为参数传递时，计算大于 GMP 编号的质数的程序。

```
<?php
// PHP program to calculate the prime  
// number greater than that of a GMP number

// creating GMP numbers using gmp_init()
$num = gmp_init(1000);

// gives the prime number just greater
// than 1000 as a GMP number
$res = gmp_nextprime($num);

echo $res;

?>
```

产出：

```
1009

```

**引用：**
[http://php.net/manual/en/function.gmp-nextprime.php](http://php.net/manual/en/function.gmp-nextprime.php)