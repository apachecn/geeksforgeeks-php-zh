# PHP | bcsub()函数

> 原文:[https://www.geeksforgeeks.org/php-bcsub-function/](https://www.geeksforgeeks.org/php-bcsub-function/)

PHP 中的 bcsub()函数是一个内置函数，用于从一个任意精度的数字中减去另一个。此函数接受两个任意精度的数字作为字符串，并在将结果缩放到指定精度后返回这两个数字的相减结果。

**语法:**

```php
*string* bcsub ( $num_str1, $num_str2, $scaleVal)
```

**参数:**该函数接受三个参数，如上面的语法所示，解释如下:

*   **$num_str1** :此参数为字符串类型，表示左操作数或我们要执行减法的两个数字之一。此参数是必需的。
*   **$num_str2** :此参数为字符串类型，表示右操作数或我们要执行减法的两个数字之一。此参数是必需的。
*   **$scaleVal** :此参数为 int 类型，可选。此参数表示加法结果中小数点后出现的位数。它的默认值为零。

**返回值:**该函数将两个数字 *$num_str1* 和 *$num_str2* 的减法作为字符串返回。

示例:

```php
Input:  $num_str1 = 11.222, $num_str2 = 3
Output: 14
Since the parameter $scaleVal is not specified so
no digits after decimal is appeared in the 
result after subtraction.

Input:  $num_str1 = 11.222, $num_str2 = 3, $scaleVal = 4
Output: 8.2220

```

下面的程序说明了 PHP 中的 bcsub()函数:

**程序 1:**

```php
<?php
// PHP program to illustrate bcsub() function

// input numbers with arbitrary precision
$num_str1 = "11.222";
$num_str2 = "3";

// calculates the subtraction of
// the two numbers when $scaleVal is
// not specified
$res = bcsub($num_str1, $num_str2);

echo $res;

?>
```

输出:

```php
8

```

**程序 2:**

```php
<?php
// PHP program to illustrate bcsub() function

// input numbers with arbitrary precision
$num_str1 = "11.222";
$num_str2 = "3";

// scale value
$scaleVal = 4;

// calculates the subtraction of the two
// numbers when $scaleVal is specified
$res = bcsub($num_str1, $num_str2, $scaleVal);

echo $res;

?>
```

输出:

```php
8.2220

```

**参考:**T2[http://php.net/manual/en/function.bcsub.php](http://php.net/manual/en/function.bcsub.php)