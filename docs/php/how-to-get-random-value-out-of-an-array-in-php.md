# PHP 中如何从数组中获取随机值？

> 原文:[https://www . geesforgeks . org/如何从 php 数组中获取随机值/](https://www.geeksforgeeks.org/how-to-get-random-value-out-of-an-array-in-php/)

PHP 中有两个函数可以从数组中获取随机值。shuffle()和 array_rand()函数用于从数组中获取随机值。

**示例:**

```
Input : $arr = ("a"=>"21", "b"=>"31", "c"=>"7", "d"=>"20")

// Get one random value
Output :7

Input : $arr = ("a"=>"21", "b"=>"31", "c"=>"7", "d"=>"20")

// Get two random values
Output : 21 31
```

**方法 1:** 该方法讨论了在 PHP 中从数组中获取随机值的 shuffle()函数。
[**PHP | shuffle()**](https://www.geeksforgeeks.org/php-shuffle-function/)**函数:**shuffle()函数是 PHP 中的一个内置函数，用于对数组中元素的顺序进行洗牌或随机化。该函数为数组中的元素分配新的键。它还将删除任何现有的键，而不仅仅是重新排序键并从零开始分配数字键。

**语法:**

```
*bool* shuffle( $array )
```

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Declare an associative array
$arr = array( "a"=>"21", "b"=>"31", "c"=>"7", "d"=>"20" );

// Use shuffle function to randomly assign numeric
// key to all elements of array.
shuffle($arr);

// Display the first shuffle element of array
echo $arr[0];

?>
```

**Output:** 

```
31
```

在上面的例子中，关联数组的键被改变了。shuffle()函数为从零开始的元素随机分配了键。As shuffle()永久更改数组的键。

**方法二:**在 PHP 中使用 array_rand()函数从数组中获取随机值。
[**PHP | array _ rand()**](https://www.geeksforgeeks.org/php-array_rand-function/)**函数:**array _ rand()函数是 PHP 中的一个内置函数，用于从数组中获取随机数量的元素。元素是一个键，可以返回一个或多个键。

**语法:**

```
array_rand( $array, $num )
```

该函数接受两个参数*$数组*和 *$num* 。$array 变量存储数组元素，$num 参数保存需要提取的元素数量。默认情况下，此参数的值为 1。

**例 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Declare an associative array
$arr = array( "a"=>"21", "b"=>"31", "c"=>"7", "d"=>"20" );

// Use array_rand function to returns random key
$key = array_rand($arr);

// Display the random array element
echo $arr[$key];

?>
```

**Output:** 

```
21
```

在上面的示例中，我们没有明确指定第二个参数的值，因此默认情况下，该值为 1，array_rand()将返回一个随机键。

**示例 2:** 本示例明确指定第二个参数的值，因此 array_rand()函数将返回随机键数组。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Declare an associative array
$arr = array( "a"=>"21", "b"=>"31", "c"=>"7", "d"=>"20" );

// It specify the number of element
$num = 2;

// It returns array of random keys
$keys = array_rand( $arr, $num );

// Display the array element
echo $arr[$keys[0]]." ".$arr[$keys[1]];

?>
```

**Output:** 

```
21 7
```