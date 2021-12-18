# PHP | ceil()函数

> 原文:[https://www.geeksforgeeks.org/php-ceil-function/](https://www.geeksforgeeks.org/php-ceil-function/)

我们经常在数学问题中使用上限函数来将一个十进制数向上舍入到下一个更大的整数值。PHP 为我们提供了一个内置函数 *ceil()* 来执行这样的操作。ceil()函数是 PHP 中的内置函数，用于将一个数字舍入到最接近的较大整数。

**语法:**

```
*float* ceil(value)
```

**参数:**ceil()函数接受单个参数*值*，该值代表要舍入到最接近的较大整数的数字。

**返回值:**ceil()函数的返回类型为 float，如语法所示。它返回代表向上舍入到下一个最高整数的*值*的数字。

示例:

```
Input : ceil(0.70)
Output : 1

Input : ceil(-4.1)
Output : -4

Input : ceil(6)
Output : 6
```

下面的程序说明了 PHP 中的 ceil()函数:

*   当带小数位的正数作为参数传递时:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

echo (ceil(0.70));

?>     
```

**输出:**

```
1
```

*   当带有小数位的负数作为参数传递时:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

echo (ceil(-4.1));

?>
```

**输出:**

```
-4
```

*   当没有小数位数的数字作为参数传递时:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

echo (ceil(6));

?>
```

**输出:**

```
6
```

**参考**:
T3】http://php.net/manual/en/function.ceil.phpT5】