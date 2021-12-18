# PHP | bcsqrt()函数

> 原文:[https://www.geeksforgeeks.org/php-bcsqrt-function/](https://www.geeksforgeeks.org/php-bcsqrt-function/)

PHP 中的 bcsqrt()函数是一个内置函数，用于计算任意精度数字的平方根。此函数接受任意精度的数字作为字符串，并在将结果缩放到指定精度后返回数字的平方根。

**语法:**

```php
*string* bcsqrt ( $num_str, $scaleVal)
```

**参数:**该函数接受三个参数，如上面的语法所示，解释如下:

*   **$num_str** :此参数为字符串类型，表示要计算平方根的操作数或数字。此参数是必需的。
*   **$scaleVal** :此参数为 int 类型，可选。此参数表示结果中小数点后出现的位数。它的默认值为零。

**返回值:**这个函数返回一个数字的平方根 *$num_str* 作为字符串。

示例:

```php
Input:  $num_str = 26
Output: 5
Since the parameter $scaleVal is not specified so
no digits after decimal is appeared in the 
result after finding out square root. 

Input:  $num_str = 26, $scaleVal = 4
Output: 5.0990

```

下面的程序说明了 PHP 中的 bcsqrt()函数:

**程序 1:**

```php
<?php
// PHP program to illustrate bcsqrt() function

// input numbers with arbitrary precision
$num_str = "26";

// calculates the square root when 
// $scaleVal is not specified
$res = bcsqrt($num_str);

echo $res;

?>
```

输出:

```php
5

```

**程序 2:**

```php
<?php
// PHP program to illustrate bcsqrt() function

// input numbers with arbitrary precision
$num_str = "26";
$scale = "4";

// calculates the square root when 
// $scaleVal is specified
$res = bcsqrt($num_str, $scale);

echo $res;

?>
```

输出:

```php
5.0990

```

**参考:**T2[http://php.net/manual/en/function.bcsqrt.php](http://php.net/manual/en/function.bcsqrt.php)