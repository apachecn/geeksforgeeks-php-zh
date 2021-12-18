# 如何用 PHP 将所有单词的第一个字符转换成大写？

> 原文:[https://www . geesforgeks . org/如何使用 php 转换所有单词的第一个字符大写/](https://www.geeksforgeeks.org/how-to-convert-first-character-of-all-the-words-uppercase-using-php/)

要将字符串中所有单词的第一个字符转换为大写，我们只需要使用一个 PHP 函数，即[**【ucwords()**。](https://www.geeksforgeeks.org/php-ucfirst-function/)

**ucwords(字符串，分隔符)**:这个函数取 2 个参数。第一个是字符串，这是强制性的。第二个参数是分隔符。

**例 1:**

## PHP

```
<?php
  echo ucwords("welcome to geeks for geeks");
?>
```

**输出**

```
Welcome To Geeks For Geeks
```

第二个参数(分隔符)是可选的。如果我们不提它，那么它会将空格后的所有单词大写。 [*回显*](https://www.geeksforgeeks.org/php-echo-print/) 关键字用于在屏幕上打印输出。

**例 2:**

## PHP

```
<?php
    // code
  echo ucwords("hey!let's get started","!")
?>
```

**输出**

```
Hey!Let's get started
```

就像“！”是分隔符，它将只大写单词“！”前后的第一个字母。

**例 3:**

## PHP

```
<?php
    // code
  $str = 'php is fun learning';
  $str = ucwords($str);
  echo $str
?>
```

**输出**

```
Php Is Fun Learning
```

为了在变量中存储字符串，我们需要在变量前面加上$符号。