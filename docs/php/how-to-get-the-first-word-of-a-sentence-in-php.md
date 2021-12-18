# 如何在 PHP 中获取一个句子的第一个单词？

> 原文:[https://www . geesforgeks . org/如何用 php 获取句子的第一个单词/](https://www.geeksforgeeks.org/how-to-get-the-first-word-of-a-sentence-in-php/)

句子的第一个单词可以通过各种内置函数来获得，比如 strtok()、strstr()、explode()和一些其他方法，比如使用正则表达式。下面列出了一些获取句子第一个单词的例子:

**方法 1:使用 [strtok()函数](https://www.geeksforgeeks.org/php-strtok-for-tokening-string/) :** 该函数用于根据给定的分隔符将字符串标记为较小的部分。它将输入字符串作为一个参数以及分隔符(作为第二个参数)。

**语法:**

```php
string strtok( $string, $delimiters )
```

**程序:**

```php
<?php
// PHP program to get the first word of
// a sentence using strtok() function

// Initialize a sentence to a variable
$sentence = 'Welcome to GeeksforGeeks';

// Use strtok() function to get the
// first word of a string
echo "The first word of string is: "
        . strtok($sentence, " ");

?> 
```

**输出:**

```php
The first word of string is: Welcome

```