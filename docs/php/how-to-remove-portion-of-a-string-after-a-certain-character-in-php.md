# 如何在 PHP 中删除字符串中某个字符后的部分？

> 原文:[https://www . geesforgeks . org/如何删除 php 中某个字符后的字符串部分/](https://www.geeksforgeeks.org/how-to-remove-portion-of-a-string-after-a-certain-character-in-php/)

substr()和 strpos()函数用于删除字符串中特定字符之后的部分。
**[strpos()函数](https://www.geeksforgeeks.org/php-strpos-stripos-functions/) :** 该函数用于查找一个字符串在另一个字符串中的第一个出现位置。函数返回字符串第一次出现的位置的整数值。函数区别对待大写和小写字符。

**语法:**

```
strpos( original_string, search_string, start_pos )
```

**返回值:**该函数返回一个整数值，代表字符串 search_str 第一次出现的 original _ str 的索引。

**[substr()函数](https://www.geeksforgeeks.org/php-substr-function/):**substr()函数是 PHP 中的一个内置函数，用于提取字符串的特定部分。

**语法:**

```
substr( string_name, start_position, string_length_to_cut )
```

**返回值:**如果成功则返回字符串的提取部分，否则返回 FALSE，如果失败则返回空字符串。
这里举几个例子。

下面的例子使用 substr()和 strpos()函数来移除字符串中特定字符之后的部分。

**例 1:**

```
<?php

// Declare a variable and initialize it
$variable = "GeeksForGeeks is the best platform.";

// Display value of variable
echo $variable;
echo "\n";

// Use substr() and strpos() function to remove
// portion of string after certain character
$variable = substr($variable, 0, strpos($variable, "is"));

// Display value of variable
echo $variable;

?>
```

**Output:**

```
GeeksForGeeks is the best platform.
GeeksForGeeks

```

**例 2:**

```
<?php

// Declare a variable and initialize it
$variable = "computer science portal for geeks";

// Display value of variable
echo $variable;
echo "\n";

// Use substr() and strpos() function to remove
// portion of string after certain character
// and display it
echo substr($variable, 0, strpos($variable, "for"));

?>
```

**Output:**

```
computer science portal for geeks
computer science portal

```