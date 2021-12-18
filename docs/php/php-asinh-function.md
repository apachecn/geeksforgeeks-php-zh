# PHP | asinh()函数

> 原文:[https://www.geeksforgeeks.org/php-asinh-function/](https://www.geeksforgeeks.org/php-asinh-function/)

在数学中，反双曲函数是双曲函数的反函数。对于双曲函数的给定值，相应的反双曲函数提供相应的双曲角。PHP 为我们提供了反双曲计算的内置函数。PHP 中的 *asinh()* 函数用于查找作为参数传递给它的数字的反双曲正弦。
**语法:**

```
*float* asinh($value)
```

**参数:**该函数接受单个参数$值。它是您想要查找其反双曲正弦值的数字。此参数的值必须以弧度为单位。
**返回值:**它返回一个浮点数，该浮点数是作为参数传递给它的数字的反双曲正弦值。
示例:

```
Input : asinh(7)
Output : 2.6441207610586

Input : asinh(56)
Output : 4.7185785811518

Input : asinh(2.45)
Output : 1.6284998192842
```

在下面的程序中，取不同的值$value 用来说明 PHP 中的 asinh()函数:

*   将 7 作为参数传递:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

echo (asinh(7));

?> 
```

*   输出:

```
2.6441207610586
```

*   将 56 作为参数传递:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

echo (asinh(56));

?>
```

*   输出:

```
4.7185785811518
```

*   将 2.45 作为参数传递:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

echo (asinh(2.45));

?>     
```

*   输出:

```
1.6284998192842
```

**参考**:
T3】http://php.net/manual/en/function.asinh.php