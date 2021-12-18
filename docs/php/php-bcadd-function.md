# PHP | bcadd()函数

> 原文:[https://www.geeksforgeeks.org/php-bcadd-function/](https://www.geeksforgeeks.org/php-bcadd-function/)

PHP 中的 bcadd()函数是一个内置函数，用于添加两个任意精度的数字。此函数接受两个任意精度的数字作为字符串，并在将结果缩放到指定精度后返回这两个数字的相加。

**语法:**

```
*string* bcadd ( $num_str1, $num_str2, $scaleVal)
```

**参数:**该函数接受三个参数，如上面的语法所示，解释如下:

*   **$num_str1** :此参数为字符串类型，表示左操作数或我们要执行加法的两个数字之一。此参数是必需的。
*   **$num_str2** :此参数为字符串类型，表示右操作数或我们要执行加法的两个数字之一。此参数是必需的。
*   **$scaleVal** :此参数为 int 类型，可选。此参数表示加法结果中小数点后出现的位数。它的默认值为零。

**返回值:**该函数将两个数字 *$num_str1* 和 *$num_str2* 相加作为字符串返回。

示例:

```
Input:  $num_str1 = 3, $num_str2 = 11.222
Output: 14
Since the parameter $scaleVal is not specified so
no digits after decimal is appeared in the 
result after addition.

Input:  $num_str1 = 3, $num_str2 = 11.222, $scaleVal = 4
Output: 14.2220

```

下面的程序说明了 PHP 中的 bcadd()函数:

**程序 1:**

```
<?php
// PHP program to illustrate bcadd() function

// input numbers with arbitrary precision
$num_str1 = "3";
$num_str2 = "11.222";

// calculates the addition of
// the two numbers when $scaleVal is
// not specified
$res = bcadd($num_str1, $num_str2);

echo $res;

?>
```

输出:

```
14

```

**程序 2:**

```
<?php
// PHP program to illustrate bcadd() function

// input numbers with arbitrary precision
$num_str1 = "3";
$num_str2 = "11.222";

// scale value
$scaleVal = 4;

// calculates the addition of the two
// numbers when $scaleVal is specified
$res = bcadd($num_str1, $num_str2, $scaleVal);

echo $res;

?>
```

输出:

```
14.2220

```

**参考:**T2[http://php.net/manual/en/function.bcadd.php](http://php.net/manual/en/function.bcadd.php)