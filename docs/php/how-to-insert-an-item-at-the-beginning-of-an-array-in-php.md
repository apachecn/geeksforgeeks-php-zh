# 在 PHP 中如何在数组的开头插入一个项目？

> 原文:[https://www . geesforgeks . org/如何在 php 数组开头插入一个项目/](https://www.geeksforgeeks.org/how-to-insert-an-item-at-the-beginning-of-an-array-in-php/)

PHP 中的数组是一种数据结构，它允许我们在一个变量下存储多个相似数据类型的元素，从而节省了我们为每个数据创建不同变量的工作量。数组有助于创建相似类型的元素列表，可以使用它们的索引或键来访问这些元素。
在数组的开头插入一个项目有两种方法，下面讨论:
**使用** [**array_merge()函数**](https://www.geeksforgeeks.org/php-merging-two-arrays-using-array_merge/)**:**array _ merge()函数用于将两个或多个数组合并为一个数组。该函数用于将两个或多个数组的元素或值合并成一个数组。

*   创建包含数组元素的数组。
*   创建另一个包含一个元素的数组，该元素需要插入到另一个数组的开头。
*   使用 array_merge()函数合并两个数组以创建一个数组。

**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Declare an array
$arr1 = array(
    "GeeksforGeeks",
    "Computer",
    "Science",
    "Portal"
);

// Declare another array containing
// element which need to insert at
// the beginning of $arr1
$arr2 = array(
    "Welcome"
);

// User array_merge() function to
// merge both array
$mergeArr = array_merge( $arr1, $arr2 );

print_r($mergeArr);

?>
```

**Output:** 

```
Array
(
    [0] => GeeksforGeeks
    [1] => Computer
    [2] => Science
    [3] => Portal
    [4] => Welcome
)
```

**使用** [**array_unshift()函数**](https://www.geeksforgeeks.org/php-array_unshift-function/)**:**array _ unshift()函数用于在数组的开头添加一个或多个元素。
**例 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Declare an array
$array = array(
    "GeeksforGeeks",
    "Computer",
    "Science",
    "Portal"
);

// Declare a variable containing element
$element = "Welcome";

// User array_unshift() function to
// insert element at beginning of array
array_unshift( $array, $element );

print_r($array);

?>
```

**Output:** 

```
Array
(
    [0] => Welcome
    [1] => GeeksforGeeks
    [2] => Computer
    [3] => Science
    [4] => Portal
)
```

**例 2:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Declare an associative array
$array = array(
    "p" => "GeeksforGeeks",
    "q" => "Computer",
    "r" => "Science",
    "s" => "Portal"
);

// Declare a variable containing element
$element = "Welcome";

// User array_unshift() function to
// insert element at beginning of array
array_unshift( $array, $element );

print_r($array);

?>
```

**Output:** 

```
Array
(
    [0] => Welcome
    [p] => GeeksforGeeks
    [q] => Computer
    [r] => Science
    [s] => Portal
)
```