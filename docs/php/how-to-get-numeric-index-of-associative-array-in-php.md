# 如何在 PHP 中获取关联数组的数值索引？

> 原文:[https://www . geesforgeks . org/如何获取 php 中关联数组的数值索引/](https://www.geeksforgeeks.org/how-to-get-numeric-index-of-associative-array-in-php/)

在 PHP 中，我们可以使用= >符号将名称/标签与每个数组元素相关联。这非常有帮助，因为很容易记住元素，因为每个元素都由标签而不是索引值来表示。
**使用 [array_keys()函数:](https://www.geeksforgeeks.org/php-array_keys-function/)**array _ keys()函数是 PHP 中的一个内置函数，用于返回数组的所有键或键的子集。

**语法:**

```
array array_keys( $input_array, $search_value, $strict )
```

**程序 1:** 使用 array_keys()函数获取关联数组的数值索引的程序。

```
<?php

// Program to print index of an associative array

// Declare an associative array
$assoc_array=array("Geeks"=>10, "for"=>15, "geeks"=>20); 

// Print index with corresponding key
// using array_keys() function
print_r(array_keys($assoc_array));

?>
```

**示例 2:** 下面的程序使用索引来访问关联数组中的值。

```
<?php

// Program to print values using index
// of associative array

// Declare an associative array
$assoc_array = array(
    "Geeks" => 30,
    "for" => 20,
    "geeks" => 10
); 

// Using array_keys() function
$key = array_keys($assoc_array);

// Calculate size of array
$size = sizeof($key);

// Using loop to access values
for( $i = 0; $i < $size; $i++) {
    echo "${assoc_array[$key[$i]]}\n";
}

?>
```