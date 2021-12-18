# PHP|max()函数

> Original: [https://www.geeksforgeeks.org/php-max-function/](https://www.geeksforgeeks.org/php-max-function/)

PHP 的*max()*函数用于查找数组中的数值最大值或几个指定值的数值最大值。 Max()函数可以接受一个数组或几个数字作为参数，并返回传递的参数中的数值最大值。 返回类型不是固定的，它可以是整数值，也可以是基于输入的浮点值。

**语法：**

```
max(array_values)  

or

max(value1, value2, ...)

```

**参数：**此函数接受两种不同类型的参数，如下所述：

1.  **ARRAY_VALUES**：它指定包含值的数组。
2.  **值 1，值 2，**…。 ：指定要比较的两个或两个以上的值。

**返回值：**max()函数返回数值上的最大值。

例如：

```
Input : max(12, 4, 62, 97, 26)
Output : 97

Input : max(array(28, 36, 87, 12))
Output : 87

```

以下程序说明了 max()在 PHP 中的工作方式：

**程序 1：**

```
<?php

echo (max(12, 4, 62, 97, 26));

?>
```

产出：

```
97
```

**程序 2**：

```
<?php

echo (max(array(28, 36, 87, 12)). "<br>");

?>
```

产出：

```
87
```

**需要注意的重要事项：**

*   Max()函数用于查找数值上的最大值。
*   Max()函数可以用于两个或两个以上的值，也可以用于数组。
*   返回的值为混合数据类型。

**参考**：
[http://php.net/manual/en/function.max.php](http://php.net/manual/en/function.max.php)