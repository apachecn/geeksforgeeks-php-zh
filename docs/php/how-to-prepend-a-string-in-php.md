# PHP 中如何前置字符串？

> 原文:[https://www . geesforgeks . org/how-prepend-a-string-in-PHP/](https://www.geeksforgeeks.org/how-to-prepend-a-string-in-php/)

我们给出了两个字符串，任务是在 PHP 中为一个字符串 **str1** 加上另一个字符串 **str2** 。在 PHP 中，没有特定的函数来预先添加字符串。为了完成这个任务，我们在 PHP 中有以下操作符:

**方法 1:使用串联运算符(“.”):**串联运算符用于通过串联 **str1** 和 **str2，将一个字符串 **str1** 与另一个字符串 **str2** 前置。**

**语法** :

```
$x . $y

```

**示例:**

## PHP

```
<?php
// PHP program to prepend a string 

// Function to prepend a string 
function prepend_string ($str1, $str2){

    // Using concatenation operator (.)
    $res = $str1 . $str2;

    // Returning the result 
    return $res;
    }

// Given string
$str1 = "Geeksforgeeks"; 
$str2 = "Example"; 

// Function Call
$str = prepend_string ($str1, $str2); 

// Printing the result
echo $str; 
?>
```

**输出**

```
GeeksforgeeksExample
```