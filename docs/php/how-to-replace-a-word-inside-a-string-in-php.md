# 如何在 PHP 中替换字符串内部的一个单词？

> 原文:[https://www . geesforgeks . org/如何在 php 中替换字符串中的单词/](https://www.geeksforgeeks.org/how-to-replace-a-word-inside-a-string-in-php/)

给定一个包含一些单词的字符串，任务是替换 PHP 中给定字符串**字符串**中出现的所有单词。为了完成这个任务，我们在 PHP 中有以下方法:

**方法 1:使用**[**str _ replace****()方法**](https://www.geeksforgeeks.org/php-str_replace-function/)**:****str _ replace()方法**用于通过替换给定字符串 **str** 中的单词 **W2** 来替换单词 **W1** 的所有出现。

**语法** :

```
str_replace( $searchVal, $replaceVal, $subjectVal, $count )

```

**示例:**

## PHP

```
<?php
// PHP program to replace all occurence
// of a word inside a string

// Given string
$str = "geeks for Geeks"; 

// Word to be replaced
$w1 = "geeks";

//  Replaced by
$w2 = "GEEKS";

// Using str_replace() function 
// to replace the word 
$str = str_replace($w1, $w2, $str);

// Printing the result
echo $str; 
?>
```

**输出**

```
GEEKS for Geeks
```