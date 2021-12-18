# PHP | bccomp()函数

> 原文:[https://www.geeksforgeeks.org/php-bccomp-function/](https://www.geeksforgeeks.org/php-bccomp-function/)

PHP 中的 bccomp()函数是一个内置函数，用于比较两个任意精度的数字。该函数接受两个任意精度的数字作为字符串，并在将两个数字比较到指定精度后返回比较结果。

**语法:**

```
*int* bccomp ( $num_str1, $num_str2, $scaleVal)
```

**参数:**该函数接受三个参数，如上面的语法所示，解释如下。

*   **$num_str1** :此参数为字符串类型，表示左操作数或我们要进行比较的两个数字之一。此参数是必需的。
*   **$num_str2** :此参数为字符串类型，表示右操作数或我们要进行比较的两个数字之一。此参数是必需的。
*   **$scaleVal** :此参数为 int 类型，可选。此参数告诉您将在比较中使用的小数点后位数。此参数的默认值为零。

**返回值:**该函数根据两个数字 *$num_str1* 和 *$num_str2* 的比较返回一个整数值。如果两个数相等，那么这个函数返回零。如果 *$num_str1* 大于 *$num_str2* 该函数返回 1，如果 *$num_str1* 小于 *$num_str2* 该函数返回-1。

示例:

```
Input:  $num_str1 = 3.22, $num_str2 = 3
Output: 0
Explanation: Since the parameter $scaleVal is not 
specified so no digits after decimal is used in 
comparison. So, the value of first parameter which 
is 3.22 will be treated as 3 and hence both 
parameters are equal.

Input:  $num_str1 = 3.222, $num_str2 = 3, $scaleVal = 2
Output: 1

Input:  $num_str1 = 3, $num_str2 = 3.222, $scaleVal = 2
Output: -1

```

下面的程序说明了 PHP 中的 bccomp()函数:

**程序 1:**

```
<?php
// PHP program to illustrate bccomp() function

// input numbers
$num_str1 = "3.12";  
$num_str2 = "3";  

// calculates the comparison of the two 
// numbers when $scaleVal is not specified
$res = bccomp($num_str1, $num_str2, 2);

// both parameters are equal
echo $res;

?>
```

输出:

```
0

```

**程序 2:**

```
<?php
// PHP program to illustrate bccomp() function

// input numbers
$num_str1 = "3.12";  
$num_str2 = "3";  

// scale value
$scaleVal = 2;

// calculates the comparison of the two 
// numbers when $scaleVal is specified
$res = bccomp($num_str1, $num_str2, $scaleVal);

// first parameter is greater than second
echo $res;

?>
```

输出:

```
1

```

**程序 3:**

```
<?php
// PHP program to illustrate bccomp() function

// input numbers
$num_str1 = "3";  
$num_str2 = "3.12";  

// scale value
$scaleVal = 2;

// calculates the comparison of the two 
// numbers when $scaleVal is specified
$res = bccomp($num_str1, $num_str2, $scaleVal);

// first parameter is smaller than second
echo $res;

?>
```

输出:

```
-1

```

**参考:**T2[http://php.net/manual/en/function.bccomp.php](http://php.net/manual/en/function.bccomp.php)