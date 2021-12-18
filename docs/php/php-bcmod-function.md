# PHP | bcmod()函数

> 原文:[https://www.geeksforgeeks.org/php-bcmod-function/](https://www.geeksforgeeks.org/php-bcmod-function/)

PHP 中的 bcmod()函数是一个内置函数，用于计算任意精度数字的模。该函数接受任意精度的数字，并在将结果缩放到指定精度后返回该数字的模。

**语法:**

```php
*string* bcadd ( $dividend, $modulus)
```

**参数:**该函数接受两个参数，如上面的语法所示，解释如下:

*   **$被除数**:该参数为字符串类型，代表被除数除以给定的模数值$ modulus。此参数是必需的。
*   **$模数**:该参数为字符串类型，代表模数。此参数是必需的。

**返回值:**当*$被除数*除以*$模数*时，该函数返回余数。换句话说，它返回的值相当于($被除数% $模数)。如果$ modulus 为零，则该函数返回空值。

示例:

```php
Input:  $dividend = 11, $modulus = 3
Output: 2

Input:  $dividend = 3, $modulus = 11
Output: 3

```

下面的程序说明了 PHP 中的 bcmod()函数:

**程序 1:**

```php
<?php
// PHP program to illustrate bcmod() function

// input numbers with arbitrary precision
$dividend = "11";
$modulus = "3";

// calculates the modulus
$res = bcmod($dividend, $modulus);

echo $res;

?>
```

输出:

```php
2

```

**程序 2:**

```php
<?php
// PHP program to illustrate bcmod() function

// input numbers with arbitrary precision
$dividend = "3";
$modulus = "11";

// calculates the modulus
$res = bcmod($dividend, $modulus);

echo $res;

?>
```

输出:

```php
3

```

**参考:**T2[http://php.net/manual/en/function.bcmod.php](http://php.net/manual/en/function.bcmod.php)