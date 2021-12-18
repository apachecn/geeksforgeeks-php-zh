# PHP 中如何统计一个字符串的字数？

> 原文:[https://www . geeksforgeeks . org/如何计算 php 中的字符串字数/](https://www.geeksforgeeks.org/how-to-count-the-number-of-words-in-a-string-in-php/)

给定一个包含一些单词的字符串，任务是在 PHP 中统计一个字符串中的单词数量  **字符串** 。为了完成这项任务，我们有以下方法:

**方法 1:使用**[**str _ word _ count****()方法**](https://www.geeksforgeeks.org/php-str_word_count-function/)**:****str _ word _ count****()**方法用于统计字符串中的字数。

**语法** :

```
str_word_count(string, return, char)

```

**示例:**

## PHP

```
<?php
// PHP program to count number of
// words in a string 

$str = "  Geeks for Geeks  "; 

// Using str_word_count() function to
// count number of words in a string
$len = str_word_count($str);

// Printing the result
echo $len; 
?>
```

**输出**

```
3
```