# 如何在 PHP 中使用 array_merge()和 array_combine()？

> 原文:[https://www . geeksforgeeks . org/如何使用 array _ merge-and-array _ combine-in-PHP/](https://www.geeksforgeeks.org/how-to-use-array_merge-and-array_combine-in-php/)

在本文中，我们将讨论如何在 PHP 中使用[**<u>【array _ merge()】</u>**](https://www.geeksforgeeks.org/php-merging-two-arrays-using-array_merge/#:~:text=The%20array_merge()%20is%20a,together%20into%20a%20single%20array.)和[**<u>array _ combine()</u>**](https://www.geeksforgeeks.org/php-array_combine-function/#:~:text=The%20array_combine()%20is%20an,values%20of%20this%20new%20array.)函数。这两个函数都是基于数组的函数，用于使用 PHP 组合两个或多个数组。我们将看到每个函数的语法和实现

**array_merge()函数:**此函数合并两个或多个数组，使所有数组都有键和值。数组附加在第一个数组的末尾。

**语法:**

```php
array_merge( array1, array2, ..., array n )
```

**参数:**数组是要合并的输入数组。

**返回类型:**合并元素的单数组。

**示例:**合并两个数组的 PHP 示例。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Define array1 with keys and values
$array1 = array(
      "subject1" => "Python",
      "subject2" => "sql"
);

// Define array2 with keys and values
$array2 = array(
      "subject3" => "c/c++",
      "subject4" => "java"
);

// Merge both array1 and array2
$final = array_merge($array1, $array2);

// Display merged array
print_r($final);

?>
```

**Output**

```php
Array
(
    [subject1] => Python
    [subject2] => sql
    [subject3] => c/c++
    [subject4] => java
)

```

**例 2:** 合并多个数组。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Define array1 with keys and values
$array1 = array(
      "subject1" => "Python",
      "subject2" => "sql"
);

// Define array2 with keys and values
$array2 = array(
      "subject3" => "c/c++",
      "subject4" => "java"
);

// Define array3 with keys and values
$array3 = array(
      "subject5" => "CN",
      "subject6" => "OS"
);

// Define array4 with keys and values
$array4 = array(
      "subject7" => "data mining",
      "subject8" => "C#"
);

// Merge all arrays
$final = array_merge($array1, 
         $array2, $array3, $array4);

// Display merged array
print_r($final);

?>
```

**Output**

```php
Array
(
    [subject1] => Python
    [subject2] => sql
    [subject3] => c/c++
    [subject4] => java
    [subject5] => CN
    [subject6] => OS
    [subject7] => data mining
    [subject8] => C#
)

```

**array_combine()函数:**此函数只组合两个数组，一个数组包含键，另一个数组包含值。

**语法:**

```php
array_combine(array1, array2)
```

**参数:**

*   array1 是第一个带键的数组。
*   array2 是第二个有值的数组。

**返回值:**返回组合数组。

**示例:** PHP 程序组合数组。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Define array1 with keys 
$array1 = array("subject1" ,"subject2");

// Define array2 with values
$array2 = array( "c/c++", "java");

// Combine two arrays
$final = array_combine($array1, $array2);

// Display merged array
print_r($final);

?>
```

**Output**

```php
Array
(
    [subject1] => c/c++
    [subject2] => java
)

```

**例 2:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Define array1 with keys 
$array1 = array("subject1", 
          "subject2", "subject3", "subject4");

// Define array2 with  values
$array2 = array( "c/c++", "java", "Python", "HTML");

// Combine two arrays
$final = array_combine($array1, $array2);

// Display merged array
print_r($final);

?>
```

**Output**

```php
Array
(
    [subject1] => c/c++
    [subject2] => java
    [subject3] => Python
    [subject4] => HTML
)

```