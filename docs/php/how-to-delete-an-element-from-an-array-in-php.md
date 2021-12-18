# 如何在 PHP 中从数组中删除一个元素？

> 原文:[https://www . geesforgeks . org/如何从 php 数组中删除元素/](https://www.geeksforgeeks.org/how-to-delete-an-element-from-an-array-in-php/)

在 PHP 中，有多种方法可以从数组中删除元素。本文讨论了 PHP 中用于从数组中删除元素的一些最常见的方法。

**使用的函数:**

*   [**unset ()**](https://www.geeksforgeeks.org/php-unset-function/) **:** This function takes an element as a parameter and unset it. It does not change the keys of other elements.
*   [**array _ splice ():**](https://www.geeksforgeeks.org/php-array_splice-function/) This function takes three parameters of an array, the offset (where to start) and the length (the number of elements to be removed). After the element is deleted, it will automatically re-index the index array, but it will not re-index the associative array.
*   [**array _ diff ():**](https://www.geeksforgeeks.org/php-array_diff-function/) **This function takes array and array value list as input, and deletes the given value from the array. Like the **unset ()** method, the keys of other elements will not be changed.**

****所用步骤:****

***   Declare a [correlation matrix](https://www.geeksforgeeks.org/associative-arrays-in-php/) .*   Delete elements from the array.*   Print the results.*   Declare an index array.*   Deletes an element from the index array.*   Print the results.**

****示例 1:** 本示例使用 **unset()** 函数删除元素。 **unset()** 函数将数组作为引用，不返回任何内容。**

## **PHP**

```php
<?php

  // Declaring associated array
  $ass_arr = ["a"=>"Geeks", "b"=>"For", "c"=>"Geeks"];

  // Deleting element associated with key "b"
  unset($ass_arr["b"]);

  // Printing array after deleting the element
  print_r($ass_arr);

  // Declaring indexed array
  $ind_arr = ["Geeks","For","Geeks"];

  // Deleting element and index 1
  unset($ind_arr[1]);

  // Printing array after deleting the element
  print_r($ind_arr);
?>
```

****输出****

```php
Array
(
    [a] => Geeks
     => Geeks
)
Array
(
    [0] => Geeks
    [2] => Geeks
)
```