# 如何在 PHP 中重置 Array？

> 原文:[https://www.geeksforgeeks.org/how-to-reset-array-in-php/](https://www.geeksforgeeks.org/how-to-reset-array-in-php/)

您可以在 PHP 中非常容易地重置数组值或清除值。有两种重置数组的方法，将在本文中进一步讨论。

**方法:**

*   [**取消设置()**](https://www.geeksforgeeks.org/php-unset-function/) 功能
*   [**array_diff()**](https://www.geeksforgeeks.org/php-array_diff-function/) 功能

**方法 1:** **unset()函数:**unset()函数用于对指定的变量或整个数组进行 unset。

**语法:**

```
unset( $variable )
```

**参数:**

*   **$变量:**此参数为必选项，是需要取消设置的变量。

**返回值:**该函数不返回值。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
$arr1 = array(
    'geeks',  
    'for', 
    'geeks' 
);

// Print the array before reset
print_r ($arr1);

// Remove item from array
unset($arr1);

// Print the reset array
var_dump($arr1);
?>
```

**输出:**

```
array(3) {
  [0]=>
  string(5) "geeks"
  [1]=>
  string(3) "for"
  [2]=>
  string(5) "geeks"
}
PHP Notice:  Undefined variable: arr1 in 
/home/159dfdccfb89fccb996feb49cfc37d39.php on line 18

NULL
```

**方法 2:** **array_diff()函数:****array _ diff()**函数接受两个或多个参数，并返回一个包含第一个数组中的值的数组，这些值在其他数组中不存在。

**语法:**

```
array_diff($array1, $array2, ..., $arrayn)
```

**参数:**函数可以取任意数量的数组作为需要比较的参数。

**返回值:**该函数将参数中的第一个数组与其余数组进行比较，并返回一个数组，该数组包含来自 *$array1* 的所有条目，这些条目在任何其他数组中都不存在。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

$array = array("Ankesh","Saurabh","Ashish","Ashu", "Anuj", "Ajinkya");

//Array before reset
print_r ($array);

// Clear the whole values of array
$array = array_diff( $array, $array);

// Array after reset
print_r ($array);

?>
```

**Output**

```
Array
(
    [0] => Ankesh
    [1] => Saurabh
    [2] => Ashish
    [3] => Ashu
    [4] => Anuj
    [5] => Ajinkya
)
Array
(
)
```