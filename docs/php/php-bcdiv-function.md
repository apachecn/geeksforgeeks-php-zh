# PHP | bcdiv()函数

> 原文:[https://www.geeksforgeeks.org/php-bcdiv-function/](https://www.geeksforgeeks.org/php-bcdiv-function/)

PHP 中的 bcdiv()函数是一个内置函数，用于划分两个任意精度的数字。此函数接受两个任意精度的数字作为字符串，并在将结果缩放到指定精度后返回这两个数字的除法。

**语法:**

```
*string* bcdiv ( $num_str1, $num_str2, $scaleVal)
```

**参数:**该函数接受三个参数，如上面的语法所示，解释如下:

*   **$num_str1** :此参数为字符串类型，代表被除数。此参数是必需的。
*   **$num_str2** :此参数为字符串类型，代表除数。此参数是必需的。
*   **$scaleVal** :此参数为 int 类型，可选。此参数表示除法结果中小数点后出现的位数。它的默认值为零。

**返回值:**该函数返回数字 *$num_str1* 除以 *$num_str2* 作为字符串。

示例:

```
Input:  $num_str1 = 11.222, $num_str2 = 3
Output: 3
Since the parameter $scaleVal is not specified so
no digits after decimal is appeared in the 
result after division.

Input:  $num_str1 = 11.222, $num_str2 = 3, $scaleVal = 4
Output: 3.7406

```

下面的程序说明了 PHP 中的 bcdiv()函数:

**程序 1:**

```
<?php
// PHP program to illustrate bcdiv() function

// input numbers
$num_str1 = "11.222";  // dividend
$num_str2 = "3";  // divisor

// calculates the division of
// the two numbers when $scaleVal is
// not specified
$res = bcdiv($num_str1, $num_str2);

echo $res;

?>
```

输出:

```
3

```

**程序 2:**

```
<?php
// PHP program to illustrate bcdiv() function

// input numbers
$num_str1 = "11.222";  // dividend
$num_str2 = "3";  // divisor

// scale value
$scaleVal = 4;

// calculates the division of the two 
// numbers when $scaleVal is specified
$res = bcdiv($num_str1, $num_str2, $scaleVal);

echo $res;

?>
```

输出:

```
3.7406

```

**参考:**T2[http://php.net/manual/en/function.bcdiv.php](http://php.net/manual/en/function.bcdiv.php)