# 如何在 PHP 中删除字符串中的所有空格？

> 原文:[https://www . geesforgeks . org/如何从 php 字符串中删除所有空格/](https://www.geeksforgeeks.org/how-to-remove-all-white-spaces-from-a-string-in-php/)

给定一个包含一些空格的字符串元素，任务是从给定的字符串**中移除所有空格。为了完成这个任务，我们在 PHP 中有以下方法:**

**方法 1:使用**[**str _ replace****()方法**](https://www.geeksforgeeks.org/php-str_replace-function/)**:****str _ replace()**方法用于通过替换给定字符串 **str** 中的字符串 **("")** 来替换搜索字符串**()**的所有出现。

**语法** :

```
str_replace($searchVal, $replaceVal, $subjectVal, $count)

```

**示例:**

## PHP

```
<?php
// PHP program to remove all white
// spaces from a string 

// Declare a string
$str = "  Geeks for   Geeks  "; 

// Using str_replace() function 
// to removes all whitespaces  
$str = str_replace(' ', '', $str);

// Printing the result
echo $str; 
?>
```

**输出**

```
GeeksforGeeks
```