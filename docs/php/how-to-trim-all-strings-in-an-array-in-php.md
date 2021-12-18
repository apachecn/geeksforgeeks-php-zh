# 如何在 PHP 中修剪数组中的所有字符串？

> 原文:[https://www . geesforgeks . org/如何修剪 php 数组中的所有字符串/](https://www.geeksforgeeks.org/how-to-trim-all-strings-in-an-array-in-php/)

给定一个带有空格的字符串数组，任务是从数组的每个对象中移除所有空格。
**例:**

```php
Input: arr = ["Geeks  ", "   for", "  Geeks  "]
Output:
Geeks
for
Geeks
```

**方法一:使用** [**修剪()**](https://www.geeksforgeeks.org/php-trim-function/) **和** [**阵 _ 走()**](https://www.geeksforgeeks.org/php-array_walk-function/) **功能:**

*   **trim()函数:**trim()函数是一个内置函数，它从字符串的左右两边删除空格和预定义的字符。
    **语法:**

```php
trim( $string, $charlist )
```

*   **array_walk()函数:**array _ walk()函数是 PHP 中的一个内置函数，它遍历整个数组而不考虑指针位置，并对数组的每个元素应用回调函数或用户定义函数。数组元素的键和值是回调函数中的参数。
    **语法:**

```php
boolean array_walk( $array, myFunction, $extraParam )
```

**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Create an array with whitespace
$arr = array( "Geeks  ", "  for", "   Geeks   ");

// Print original array
echo "Original Array:\n";
foreach($arr as $key => $value)
    print($arr[$key] . "\n");

// Iterate array through array_walk() function
// and use trim() function to remove all
// whitespaces from every array objects
array_walk($arr, create_function('&$val',
                    '$val = trim($val);'));

// Print modify array
echo "\nModified Array:\n";
foreach($arr as $key => $value)
    print($arr[$key] . "\n");

?>
```

**Output:** 

```php
Original Array:
Geeks  
  for
   Geeks   

Modified Array:
Geeks
for
Geeks
```

**方法二:使用** [**修剪()**](https://www.geeksforgeeks.org/php-trim-function/) **和** [**阵 _ 图()**](https://www.geeksforgeeks.org/php-array_map-function/) **功能:**

*   array_map()函数是 PHP 中的一个内置函数，它有助于根据用户定义的条件以简单的方式修改一个或多个数组中的所有元素。基本上，它将数组的每个元素发送给用户定义的函数，并返回一个带有该函数修改后的新值的数组。
    **语法:**

```php
array_map(functionName, arr1, arr2...)
```

**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Create an array with whitespace
$arr = array( "Geeks  ", "  for", "   Geeks   ");

// Print original array
echo "Original Array:\n";
foreach($arr as $key => $value)
    print($arr[$key] . "\n");

// Iterate array through array_map() function
// Using trim() function to remove all
// whitespaces from every array objects
$arr = array_map('trim', $arr);

// Print modify array
echo "\nModified Array:\n";
foreach($arr as $key => $value)
    print($arr[$key] . "\n");

?>
```

**Output:** 

```php
Original Array:
Geeks  
  for
   Geeks   

Modified Array:
Geeks
for
Geeks
```

**方法 3:使用 for 循环的基本方法:**使用 for 循环遍历数组的每个元素，然后使用 trim()函数从数组元素中移除所有空白。
**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Create an array with whitespace
$arr = array( "Geeks  ", "  for", "   Geeks   ");

// Print original array
echo "Original Array:\n";
foreach($arr as $key => $value)
    print($arr[$key] . "\n");

// Print modify array
echo "\nModified Array:\n";

// Iterate array through for loop
// Using trim() function to remove all
// whitespaces from every array objects
foreach($arr as $key => $value) {
    $arr[$key] = trim($value);

    // Print current object of array
    print($arr[$key] . "\n");
}

?>
```

**Output:** 

```php
Original Array:
Geeks  
  for
   Geeks   

Modified Array:
Geeks
for
Geeks
```