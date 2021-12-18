# 如何在 PHP 中获取数组中使用的元素总数？

> 原文:[https://www . geesforgeks . org/如何获取 php 数组中使用的元素总数/](https://www.geeksforgeeks.org/how-to-get-total-number-of-elements-used-in-array-in-php/)

在本文中，我们将讨论如何从数组中获取 PHP 中的元素总数。我们可以通过使用[**<u>count()</u>**](https://www.geeksforgeeks.org/php-count-function/)<u>和[**<u>sizeof()</u>**](https://www.geeksforgeeks.org/php-sizeof-function/)函数来获取数组中元素的总数。</u>

<u>**使用** [**count()函数:**](https://www.geeksforgeeks.org/php-count-function/)**count()函数用于获取数组中元素的总数。**</u>

<u>****语法:****</u>

```php
**count(array)**
```

<u>****参数:**它接受单个参数，即作为输入数组的数组。**</u>

<u>****返回值:**返回数组中元素的个数。**</u>

<u>****程序 1:** 使用 count()函数对数组中的元素进行计数的 PHP 程序。**</u>

## <u>**服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**</u>

```php
**<?php

// Create an associative array 
// with 5 subjects
$array1 = array(
      0 => 'php',  
      1 => 'java',  
      2 => 'css/html', 
      3 => 'python',
      4 => 'c/c++'
);

// Get total elements in array
echo count( $array1);

?>**
```

<u>****Output**

```php
5
```**</u> 

<u>**[**sizeof()函数**](https://www.geeksforgeeks.org/php-sizeof-function/)**:**sizeof()函数用于计算数组或任何其他可计数对象中存在的元素数量。**</u>

<u>****语法:****</u>

```php
**sizeof(array)**
```

<u>****参数:**它只接受一个参数数组，即输入数组。**</u>

<u>****返回值:**返回数组中存在的元素个数。**</u>

<u>****示例:****</u>

```php
**Input: array(10,20,30,50)
Output: 4

Input: array("Hello","geeks")
Output: 2**
```

<u>****程序 2:** PHP 程序使用 sizeof()函数对元素个数进行计数。**</u>

## <u>**服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**</u>

```php
**<?php

// Create an associative array
// with 5 subjects
$array1 = array(
      0 => 'php',  
    1 =>'java',  
      2 => 'css/html', 
      3 => 'python',
      4 => 'c/c++'
);

// Get total elements in array
echo sizeof( $array1);

?>**
```

<u>****Output**

```php
5
```**</u>