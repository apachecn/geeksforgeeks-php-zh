# 如何在 PHP 中追加字符串？

> 原文:[https://www . geesforgeks . org/如何在 php 中追加字符串/](https://www.geeksforgeeks.org/how-to-append-a-string-in-php/)

我们给了两个字符串，任务是 给追加一个字符串 **str1** 加上另一个字符串 **str2** 在 PHP 中。在 PHP 中追加一个字符串没有特定的功能。 为了完成这个任务，我们在 PHP 中有这个操作符:

**使用** **串联赋值** **运算符** **()。=”:**串联赋值 运算符用于将一个字符串 **str1** 附加到另一个字符串 **str2。**T21】

**语法** :

```php
$x .= $y

```

**示例:**

## PHP

```php
<?php
// PHP program to append a string 

// function to append a string 
function append_string ($str1, $str2) {

    // Using Concatenation assignment
    // operator (.=)
    $str1 .=$str2;

    // Returning the result 
    return $str1;
}

// Given string
$str1 = "Geeks"; 
$str2 = "for"; 
$str3 = "Geeks"; 

// function calling
$str = append_string ($str1, $str2);
$str = append_string ($str, $str3);

// Printing the result
echo $str; 
?>
```

**输出**

```php
GeeksforGeeks
```