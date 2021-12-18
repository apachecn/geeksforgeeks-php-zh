# 如何用 PHP 只删除字符串开头/结尾的空格？

> 原文:[https://www . geesforgeks . org/how-to-remove-white-spaces-only-start-end-a-string-use-PHP/](https://www.geeksforgeeks.org/how-to-remove-white-spaces-only-beginning-end-of-a-string-using-php/)

我们给了一个字符串，任务是只从字符串的开头或者从字符串的结尾删除空格，在 PHP 中是**字符串**。为了完成这个任务，我们在 PHP 中有以下方法:

**方法 1:使用** [**ltrim()方法**](https://www.geeksforgeeks.org/php-ltrim-function/)**:****ltrim()**方法 仅用于从字符串的**开头去除空白。**

**语法** :

```php
ltrim($string, $charlist)

```

**示例:**

## PHP

```php
<?php
// PHP program to remove white space
// from beginning of a string 

$str = "  Geeks  for  Geeks   "; 

// Using ltrim() function 
// removes whitespaces from 
// beginning of a string 
$str = ltrim($str);

// Printing the result
echo $str; 

$len = strlen($str);

echo "\nLength of String: ";  
echo $len;
?>
```

**输出**

```php
Geeks  for  Geeks   
Length of String: 20
```