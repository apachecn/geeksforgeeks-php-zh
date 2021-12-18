# PHP | bcpow()函数

> 原文:[https://www.geeksforgeeks.org/php-bcpow-function/](https://www.geeksforgeeks.org/php-bcpow-function/)

PHP 中的 bcpow()函数是一个内置函数，用于计算提升到另一个指数的任意精度基数的值。此函数接受两个任意精度的数字作为字符串，并在将结果缩放到指定精度后返回提升到指数的基数。

**语法:**

```php
*string* bcpow ( $base, $exponent, $scaleVal )
```

**参数:**该函数接受三个参数，如上面的语法所示，解释如下:

*   **$base** :此参数为字符串类型，代表将提升功率的基数。此参数是必需的。
*   **$指数**:该参数为字符串类型，代表指数。此参数是必需的。
*   **$scaleVal** :此参数为 int 类型，可选。该参数表示基数<sup>指数</sup>结果中小数点后出现的位数。它的默认值为零。

**返回值:**该函数将$ base<sup>$ index</sup>结果作为字符串返回。

示例:

```php
Input:  $base = 2, $exponent = 3 
Output: 8
Since the parameter $scaleVal is not specified so
no digits after decimal is appeared in the 
result after evaluating result

Input:  $base = 2, $exponent = 3, $scaleVal = 2
Output: 8
Note: Instead of 8.00, output of 8 is given. 
This is an exception in bc math functions.

```

下面的程序说明了 PHP 中的 bcpow()函数:

**程序 1:**

```php
<?php
// PHP program to illustrate bcpow() function

// input numbers with arbitrary precision
$base = "2";
$exponent = "3"; 

// calculates the base^exponent
// the two numbers when $scaleVal is
// not specified
$res = bcpow($base, $exponent);

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
// PHP program to illustrate bcpow() function

// input numbers with arbitrary precision
$base = "2";
$exponent = "3";

// scale value
$scaleVal = 4;

// calculates the base^exponent
// the two numbers when $scaleVal is
// specified 
$res = bcpow($base, $exponent, $scaleVal); 

echo $res;
?>
```

输出:

```php
2

```

**参考:**T2[http://php.net/manual/en/function.bcpow.php](http://php.net/manual/en/function.bcpow.php)