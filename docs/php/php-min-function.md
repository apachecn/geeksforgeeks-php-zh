# PHP|min()函数

> Original: [https://www.geeksforgeeks.org/php-min-function/](https://www.geeksforgeeks.org/php-min-function/)

PHP 的*min()*函数用于查找数组中的最低值，或几个指定值中的最低值。 Min()函数可以接受一个数组或几个数字作为参数，并返回传递的参数中数值最小的值。 返回类型不是固定的，它可以是整数值，也可以是基于输入的浮点值。

**语法：**

```php
min(array_values)  

or

min(value1, value2, ...)

```

**参数：**此函数接受两种不同类型的参数，具体说明如下：

1.  **ARRAY_VALUES**：它指定包含值的数组。
2.  **值 1，值 2，**…。 ：指定要比较的两个或两个以上的值。

**返回值：**min()函数返回数值上的最小值。

例如：

```php
Input : min(12, 4, 62, 97, 26)
Output : 4

Input : min(array(28, 36, 87, 12))
Output : 12

```

以下程序说明了 min()在 PHP 中的工作方式：

**程序 1：**

```php
<?php

echo (min(12, 4, 62, 97, 26));

?>
```

产出：

```php
4
```

**程序 2：**

```php
<?php

echo (min(array(28, 36, 87, 12)));

?>
```

产出：

```php
12
```

**需要注意的重要事项：**

*   Min()函数用于查找数值最小的数字。
*   Min()函数可以用于两个或两个以上的值，也可以用于数组。
*   返回的值为混合数据类型。

**参考**：
[http://php.net/manual/en/function.min.php](http://php.net/manual/en/function.min.php)