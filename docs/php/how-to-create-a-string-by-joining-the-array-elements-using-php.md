# 如何用 PHP 连接数组元素创建字符串？

> 原文:[https://www . geesforgeks . org/如何通过使用 php 连接数组元素来创建字符串/](https://www.geeksforgeeks.org/how-to-create-a-string-by-joining-the-array-elements-using-php/)

我们给出了一个包含一些数组元素的数组，任务是将所有的数组元素连接成一个字符串。为了完成这个任务，我们在 PHP 中有以下方法:

**方法 1:使用** [**内爆()方法**](https://www.geeksforgeeks.org/php-implode-function/)**:****内爆()** 方法 用于连接由字符串分隔的元素数组。连接可以在有或没有隔板的情况下进行。

**语法** :

```php
*string* implode($separator, $array)

```

**示例:**

## PHP

```php
<?php
// PHP program to create a string by 
// joining the values of an array

// Function to get the string 
function get_string ($arr) {

    // Using implode() function to
    // join without separator 
    echo implode($arr); 

    // Using implode() function to
    // join with separator 
    echo implode("-", $arr); 
}

// Given array
$arr = array('Geeks','for','Geeks',"\n");

// function calling
$str = get_string ($arr); 
?>
```

**输出**

```php
GeeksforGeeks
Geeks-for-Geeks-

```