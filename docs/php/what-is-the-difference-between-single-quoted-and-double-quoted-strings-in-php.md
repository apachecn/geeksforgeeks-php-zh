# PHP 中单引号和双引号字符串有什么区别？

> 原文:[https://www . geesforgeks . org/PHP 中单引号和双引号字符串的区别是什么/](https://www.geeksforgeeks.org/what-is-the-difference-between-single-quoted-and-double-quoted-strings-in-php/)

PHP 编程中的单引号或双引号用于定义字符串。但是，这两者之间有很多不同之处。

**单引号字符串:**这是定义字符串最简单的方法。当您希望字符串完全如其所写时，可以使用它。所有的转义序列，如 **\r** 或 **\n** ，将按指定输出，而不具有任何特殊含义。在某些情况下，单引号通常更快。特殊情况是，如果要显示文字单引号，可以用**反斜杠(\)** 转义，如果要显示反斜杠，可以用另一个**反斜杠(\\)** 转义。

下面的程序说明了**单引号字符串:**
**程序 1:**

```
<?php

// A simple string
echo 'I am a geek. ';
echo"\n";

// use of back-slash to display string with apostrophe
echo 'It\'ll be interesting to know about the string. ';
echo"\n";

// to escape the backslash within the string
echo 'A \\ is named as backslash. ';
echo"\n";

// The variable will not be evaluated if used directly
//within the single-quoted string
$string = 'geeks';
echo 'This is a portal for $string. ';
echo"\n";

// The \n will be displayed as it is without having any
//special meaning.
echo 'This is a portal for \n geeks. ';
?>
```

输出:

```
I am a geek. 
It'll be interesting to know about the string. 
A \ is named as backslash. 
This is a portal for $string. 
This is a portal for \n geeks.
```

**双引号字符串:**通过使用双引号，PHP 代码被迫计算整个字符串。双引号和单引号的主要区别在于，通过使用双引号，可以直接在字符串中包含变量。它解释转义序列。每个变量都将被其值替换。

下面的程序说明了**双引号字符串:**
**程序 2:**

```
<?php

// A simple string.
echo "I am a geek.";

echo"\n";

// Nothing extra is needed here
echo "It'll be interesting to know about the string.";

echo"\n";

// \n is working here
echo "This is a simple string.";

echo"\n";

// Variables are included directly
$string = 'ABC';
echo "The word is $string.";

?>
```

输出:

```
I am a geek.
It'll be interesting to know about the string.
This is a simple string.
The word is ABC.

```