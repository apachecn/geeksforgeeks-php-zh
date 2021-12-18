# PHP | array_splice()函数

> 原文:[https://www.geeksforgeeks.org/php-array_splice-function/](https://www.geeksforgeeks.org/php-array_splice-function/)

PHP 的这个内置函数是 [array_slice()](https://www.geeksforgeeks.org/php-array_slice-function/) 函数的高级扩展版本，我们不仅可以从数组中移除元素，还可以向数组中添加其他元素。该函数通常用其他数组中的元素替换现有元素，并返回已移除或替换元素的数组。

**语法:**

```php
*array* array_splice($array1, $start_point, $range, $array2)
```

**参数:**这个函数可以取四个参数，描述如下:

1.  **$array1(必选):**这个参数指的是原始数组，我们要对其进行操作。
2.  **$start_point(必选):**此参数是指数组中需要移除元素的起始位置。必须提供该值。如果提供的值为负，则函数开始从数组末尾移除，即-1 表示数组的最后一个元素。
3.  **$range(可选):**该参数是指需要进行移除的范围或极限点。负值将指示从字符串末尾开始的计数。现在，这个也可以留空。如果留空，该函数将删除从起点到终点的所有值。
4.  **$array2(可选):**这是指另一个数组，其元素将被插入到$array1 中。现在为了插入一个元素，我们不需要提供整个数组。我们可以只为一个值传递一个字符串。对于值组，我们需要一个数组。

**返回值:**该函数将从$start_point 到$range 返回一个已删除元素的数组。

下面的程序说明了 PHP 中的 array_splice()函数:

```php
<?php

// PHP program to illustrate the use 
// of array_splice() function

$array1 = array("10"=>"raghav", "20"=>"ram", 
    "30"=>"laxman","40"=>"aakash","50"=>"ravi");

$array2 = array("60"=>"ankita","70"=>"antara");

echo "The returned array: \n";
print_r(array_splice($array1, 1, 4, $array2));

echo "\nThe original array is modified to: \n";
print_r($array1);

?>
```

输出:

```php
The returned array: 
Array
(
    [0] => ram
    [1] => laxman
    [2] => aakash
    [3] => ravi
)

The original array is modified to: 
Array
(
    [0] => raghav
    [1] => ankita
    [2] => antara
)
```

**参考**:
T3】http://php.net/manual/en/function.array-splice.php