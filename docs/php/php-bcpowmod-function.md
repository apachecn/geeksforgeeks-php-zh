# PHP | bcpowmod()函数

> 原文:[https://www.geeksforgeeks.org/php-bcpowmod-function/](https://www.geeksforgeeks.org/php-bcpowmod-function/)

PHP 中的 bcpowmod()函数是一个内置函数，用于将任意精度的基数提升到另一个指数数，再降低一个指定的模数。此函数接受三个任意精度的数字作为字符串，并在将结果缩放到指定精度后，返回在一个数字下提升到指数模的基数。

**语法:**

```
*string* bcpowmod ( $base, $exponent, $mod, $scaleVal )
```

**参数:**该函数接受四个参数，如上面的语法所示，解释如下:

*   **$base** :此参数为字符串类型，表示左操作数或数字，该数字是乘幂的基数。此参数是必需的。
*   **$指数**:该参数为字符串类型，代表右操作数或代表指数的数字之一。此参数是必需的。
*   **$mod** :该参数为字符串类型，接受代表 modulos 的操作数或数字。此参数是必需的。
*   **$scaleVal** :此参数为 int 类型，可选。此参数告诉(基数<sup>指数</sup> )%mod 的结果中小数点后出现的位数。它的默认值为零。

**返回值:**该函数返回字符串形式的$(基数<sup>$指数</sup> ) % $mod 结果。

示例:

```
Input:  $base = 2, $exponent = 3 $mod = 3
Output: 2
Since the parameter $scaleVal is not specified so
no digits after decimal is appeared in the 
result after evaluating result

Input:  $base = 2, $exponent = 3, $mod = 3, $scaleVal = 2
Output: 2.00

```

下面的程序说明了 PHP 中的 bcpowmod()函数:

**程序 1:**

```
<?php
// PHP program to illustrate bcpowmod() function

// input numbers with arbitrary precision
$base = "2";
$exponent = "3"; 
$mod = "3";

// calculates the base^exponent % mod
// when $scaleVal is not specified
$res = bcpowmod($base, $exponent, $mod);

echo $res;

?>
```

输出:

```
2

```

**程序 2:**

```
<?php
// PHP program to illustrate bcpowmod() function

// input numbers with arbitrary precision
$base = "2";
$exponent = "3";
$mod = "3";

// scale value
$scaleVal = 4;

// calculates the base^exponent % mod
// when $scaleVal is specified 
$res = bcpowmod($base, $exponent, $mod, $scaleVal); 

echo $res;

?>
```

输出:

```
2.0000

```

**参考:**T2[http://php.net/manual/en/function.bcpowmod.php](http://php.net/manual/en/function.bcpowmod.php)