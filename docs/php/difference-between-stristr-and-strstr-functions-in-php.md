# PHP 中 stristr()和 strstr()函数的区别

> 原文:[https://www . geesforgeks . org/stristr-和-strtr-functions-in-PHP/](https://www.geeksforgeeks.org/difference-between-stristr-and-strstr-functions-in-php/)之间的区别

字符串是存储在一起的字符序列。它可能包含数字、字符或特殊字符。可以搜索和修改字符串。这两个 PHP 函数[**strtr()**](https://www.geeksforgeeks.org/php-strstr-function/)和 [**stristr()**](https://www.geeksforgeeks.org/php-stristr-function/) 都是用来在另一个字符串中搜索一个字符串的。

**strtr()方法:**[**strtr()**](https://www.geeksforgeeks.org/php-strstr-function/)方法用于以不区分大小写的方式搜索另一个字符串中的字符串。这个函数被认为是二进制安全的。

**语法:**

```
strstr(string, search, before_search)
```

**参数:**

*   **String:** The string where the search string is located.
*   **Search:** Search parameter, character string or number to be located.
*   [T0】 before _ search: 【T1] The default value is *false* . If set to *True* , the part of the string before the first occurrence of the search parameter is returned.

**示例 1:** 以下代码片段指示使用整数作为搜索参数。“a”的 [ASCII](https://www.geeksforgeeks.org/ascii-table/) 代码是 97，因此，“e”的值相当于 101。因此，将返回第一次出现字符“e”之后的字符串以及该字符。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
$asciich = 101;

echo strstr("GeeksforGeeks!", $asciich);

?>
```

**Output**

```
eeksforGeeks!
```

**例 2:**

## PHP

```
<?php

$find = "GeEks";

echo("String after the first occurrence : ");
echo strstr("Here is geeks for GeEks!", $find);
echo('</br>');
echo("String before the first occurrence : ");
echo strstr("Here is geeks for GeEks!", $find, true);

?>
```

**输出:**

```
String after the first occurrence : GeEks!
String before the first occurrence : Here is geeks for
```

**stristr()方法:**[**stristr()**](https://www.geeksforgeeks.org/php-stristr-function/)方法用于以区分大小写的方式搜索另一个字符串内部的字符串。这个函数被认为是二进制安全的。

**语法:**

```
stristr(string, search, before_search)
```

**参数:**

*   **String:** The string where the search string is located.
*   **Search:** Search parameters, that is, strings or numbers to be located.
*   [T0】 before _ search: 【T1] The default value is false. If set to true, it will return the part of the string before the first occurrence of the search. Parameters.

**例:**

## PHP

```
<?php

$find = "GEEKS";

echo("String after the first occurrence : ");
echo stristr("Here is geeks for geeks!", $find);
echo('</br>');
echo("String before the first occurrence : ");
echo stristr("Here is geeks for geeks!", $find, true);

?>
```

**输出:**

```
String after the first occurrence : geeks for geeks!
String before the first occurrence : Here is
```

**注意:**T2 strstr()和 **stristr()** 方法唯一的区别是**str()**方法不区分大小写， **stristr()** 方法区分大小写。