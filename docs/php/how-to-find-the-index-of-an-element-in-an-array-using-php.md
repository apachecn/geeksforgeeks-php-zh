# 如何用 PHP 找到数组中某个元素的索引？

> 原文:[https://www . geesforgeks . org/如何使用 php 找到数组中元素的索引/](https://www.geeksforgeeks.org/how-to-find-the-index-of-an-element-in-an-array-using-php/)

在本文中，我们将讨论如何在 PHP 中找到数组中元素的索引。数组索引从 0 到 n-1 开始。我们可以通过使用[**<u>array _ search()</u>**T5】函数来获取数组索引。该函数用于搜索给定的元素。它将接受两个参数。](https://www.google.com/amp/s/www.geeksforgeeks.org/php-array_search-function/amp/)

**语法:**

```php
array_search('element', $array)
```

**参数:**

*   第一个是数组中的元素。
*   第二个是数组名。

**返回值:**返回整数的索引号。

**注意:**我们将从索引数组和关联数组中获取索引。

**示例 1:** 从索引数组中获取特定元素索引的 PHP 程序。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Create an indexed array with 5 subjects
$array1 = array('php', 'java', 
         'css/html', 'python', 'c/c++');

// Get the index of PHP
echo array_search('php', $array1);
echo "\n";

// Get the index of java
echo array_search('java', $array1);
echo "\n";

// Get the index of c/c++
echo array_search('c/c++', $array1);
echo "\n";

?>
```

**Output**

```php
0
1
4

```

**示例 2:** 以下示例返回关联数组的索引。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Create an associative array
// with 5 subjects
$array1 = array(
      0 => 'php', 
      1 => 'java',
      2 => 'css/html', 
      3 => 'python',
      4 => 'c/c++'
);

// Get the index of php
echo array_search('php', $array1);
echo "\n";

// Get the index of java
echo array_search('java', $array1);
echo "\n";

// Get index of c/c++
echo array_search('c/c++', $array1);
echo "\n";

?>
```

**Output**

```php
0
1
4

```