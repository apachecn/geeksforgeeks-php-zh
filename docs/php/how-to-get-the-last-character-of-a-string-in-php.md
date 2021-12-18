# 如何在 PHP 中获取字符串的最后一个字符？

> 原文:[https://www . geesforgeks . org/如何获取 php 中字符串的最后一个字符/](https://www.geeksforgeeks.org/how-to-get-the-last-character-of-a-string-in-php/)

在本文中，我们将找到 PHP 中字符串的最后一个字符。使用以下方法可以找到最后一个字符。

*   Use [**array ()**](https://www.geeksforgeeks.org/php-array-function/) [](https://www.geeksforgeeks.org/php-substr-function/)method.
*   [基底()T3](https://www.geeksforgeeks.org/php-substr-function/)

**使用** [**数组()**](https://www.geeksforgeeks.org/php-array-function/) **方法:**在这个方法中，我们会找到字符串的长度，然后打印(length-1)的值。例如，如果字符串是“Akshit”，它的长度是 6，在零索引中，(length-1)的值是 5，这是字符“t”。长度可以使用 PHP**[**strlen()**](https://www.geeksforgeeks.org/php-strlen-function/)方法找到。**

**strlen()是 PHP 中的一个内置函数，它返回给定字符串的长度。它将字符串作为参数并返回其长度。它计算字符串的长度，包括所有空格和特殊字符。**

****语法:****

```php
strlen($string)
```

****示例:****

## **服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**

```php
<?php
 $txt = "Geeksforgeeks";
 echo "Last Character of string is : " 
   .$txt[strlen($txt)-1];
?>
```

****输出:****

```php
Last Character of string is : s
```

****使用** [**substr()**](https://www.geeksforgeeks.org/php-substr-function/) **方法:**substr()是 PHP 中的内置函数，用于提取字符串的一部分。**

****语法:****

```php
substr(string_name, start_position, string_length_to_cut)
```

****举例:**比如，如果字符串是“Akshit 爱 GeeksForGeeks”。字符串的最后一个字符是“s”。有 2 种方法可以达到“s”。从一开始“s”就排在第 25 位。我们可以找到字符串的长度，然后显示“length-1”。这意味着我们希望使用 **substr()** 方法显示字符串的一部分，其中起点是“length-1”。**

 **## PHP

```php
<?php
$txt = "Akshit Loves GeeksForGeeks";
echo "Last character of String is : "
  .substr($txt, strlen($txt)-1);
?>
```** 

****输出:**从最后看，“s”排在第 1 位。我们可以显示从(-1)**

```php
Last character of String is : s
```

**开始的字符串

**从结束:**“s”在第一位置

我们可以从“-1”

## PHP

```php
<?php
$txt = "Akshit Loves GeeksForGeeks";
echo "Last character of String is: ".substr($txt, -1);
?>
```

**输出**

```php
Last character of String is: s
```

**注意:**如果您使用的是像 UTF-8 这样的多字节字符编码，请使用 **mb_substr()** 而不是 substr。**