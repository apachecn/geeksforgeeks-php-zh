# 如何用 PHP 去除数组中的重复值？

> 原文:[https://www . geesforgeks . org/如何使用 php 从数组中删除重复值/](https://www.geeksforgeeks.org/how-to-remove-duplicate-values-from-array-using-php/)

在本文中，我们将讨论如何在 PHP 中移除数组中的重复元素。我们可以通过使用 [***阵 _ 独特()***T5】功能来获取独特元素。该函数将从数组中删除重复的值。](https://www.geeksforgeeks.org/php-array_unique-function/)

**语法:**

```
array array_unique($array, $sort_flags)
```

**注意:**数组的键被保留，即输入数组中未移除元素的键在输出数组中将是相同的。

**参数:**该函数接受下面讨论的两个参数:

*   **$array:** 此参数是必须提供的，它指定了我们要从中删除重复项的输入数组。
*   **$sort_flags:** 为可选参数。此参数可用于使用以下值修改排序行为:
    *   **SORT_REGULAR:** 这是参数$sort_flags 的默认值。该值告诉函数正常比较项目(不要改变类型)。
    *   **SORT_NUMERIC:** 该值告诉函数对项目进行数值比较。
    *   **SORT_STRING:** 该值告诉函数将项目作为字符串进行比较。
    *   **SORT_LOCALE_STRING:** 该值告诉函数根据当前的区域设置将项目作为字符串进行比较。

**返回值:**array _ unique()函数在从数组中移除所有重复项后返回过滤后的数组。

**示例:**从数组中移除重复值的 PHP 程序。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Input Array
$a = array("red", "green", "red", "blue");

// Array after removing duplicates
print_r(array_unique($a));

?>
```

**Output**

```
Array
(
    [0] => red
    [1] => green
    [3] => blue
)
```

**示例 2:** 从关联数组中移除重复元素的 PHP 程序。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Input array
$arr = array(
      "a" => "MH", 
      "b" => "JK", 
      "c" => "JK", 
      "d" => "OR"
);

// Array after removing duplicates
print_r(array_unique($arr));

?>
```

**Output**

```
Array
(
    [a] => MH
    [b] => JK
    [d] => OR
)
```