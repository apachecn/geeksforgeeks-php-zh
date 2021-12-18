# PHP | array_product()函数

> 原文:[https://www.geeksforgeeks.org/php-array_product-function-2/](https://www.geeksforgeeks.org/php-array_product-function-2/)

**array_product()** 是 PHP 中的一个内置函数，它返回给定数组中所有数字的乘积。该函数接受仅由数字组成的数组。如果数组中除了数字还有其他数据，函数返回 0。

**语法:**

```
array_product($array)
```

**参数:**函数有一个强制参数$array，我们要为其计算所有值的乘积。

**返回值:**该函数根据以下情况返回三个不同的值:

*   如果数组至少包含一个非数字数据，则返回 0。
*   当空数组作为参数传递时，它返回 1。
*   如果以上两种情况都不满足，那么它返回数组中所有项的乘积。

示例:

```
Input : $array = [1, 2, 3, 4]
Output : 24 

Input : $array = [1, 'a'] 
Output : 0 

```

下面的程序说明了 array_product()函数:

**程序 1:** 演示 array_product()函数的程序。

```
<?php
// PHP program to demonstrate 
// the array_product() function
$a1=array(1, 2, 3, 4);

echo(array_product($a1));
?>
```

**输出:**

```
24
```

**程序 2:** 当数组至少包含一个非数字数据时，演示 array_product()函数的程序。

```
<?php
// PHP program to demonstrate the array_product() 
// function when the array contains at least
// one non-number data

$a1=array(1, 2, 3, 'a');

echo(array_product($a1));
?>
```

**输出:**

```
0
```

**程序 3:** 程序演示数组为空时的 array_product()函数。

```
<?php
// PHP program to demonstrate the array_product() function
// when the array is empty

$a1=array();

echo(array_product($a1));
?>
```

**输出:**

```
1
```

**参考**:
T3】http://php.net/manual/en/function.array-product.php