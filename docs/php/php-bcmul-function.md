# PHP | bcmul()函数

> 原文:[https://www.geeksforgeeks.org/php-bcmul-function/](https://www.geeksforgeeks.org/php-bcmul-function/)

PHP 中的 bcmul()函数是一个内置函数，用于乘以两个任意精度的数字。此函数接受两个任意精度的数字作为字符串，并在将结果缩放到指定精度后返回这两个数字的乘积。

**语法:**

```
*string* bcmul ( $num_str1, $num_str2, $scaleVal)
```

**参数:**该函数接受三个参数，如上面的语法所示，解释如下:

*   **$num_str1** :此参数为字符串类型，表示左操作数或我们要执行乘法的两个数字之一。此参数是必需的。
*   **$num_str2** :此参数为字符串类型，表示右操作数或我们要执行乘法的两个数字之一。此参数是必需的。
*   **$scaleVal** :此参数为 int 类型，可选。此参数表示乘法结果中小数点后出现的位数。它的默认值为零。

**返回值:**该函数将两个数字 *$num_str1* 和 *$num_str2* 的乘积作为字符串返回。

示例:

```
Input:  $num_str1 = 3, $num_str2 = 11.222
Output: 33
Explanation: Since the parameter $scaleVal is not 
specified so no digits after decimal is appeared 
in the result after multiplication.

Input:  $num_str1 = 3, $num_str2 = 11.222, $scaleVal = 4
Output: 36.6660

```

下面的程序说明了 PHP 中的 bcmul()函数:

**程序 1:**

```
<?php
// PHP program to illustrate bcmul() function

// input numbers with arbitrary precision
$num_str1 = "3";
$num_str2 = "11.222";

// calculates the multiplication of the two
// numbers when $scaleVal is not specified
$res = bcmul($num_str1, $num_str2);

echo $res;

?>
```

输出:

```
33

```

**程序 2:**

```
<?php
// PHP program to illustrate bcmul() function

// input numbers with arbitrary precision
$num_str1 = "3";
$num_str2 = "11.222";

// scale value
$scaleVal = 3;

// calculates the multiplication of the two
// numbers when $scaleVal is specified
$res = bcmul($num_str1, $num_str2, $scaleVal);

echo $res;

?>
```

输出:

```
33.666

```

**参考:**T2[http://php.net/manual/en/function.bcmul.php](http://php.net/manual/en/function.bcmul.php)