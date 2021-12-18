# PHP 中如何替换 String？

> 原文:[https://www.geeksforgeeks.org/how-to-replace-string-in-php/](https://www.geeksforgeeks.org/how-to-replace-string-in-php/)

在本文中，我们将使用 PHP 内置的 [**str_replace()**](https://www.geeksforgeeks.org/php-str_replace-function/) 函数来用另一个字符串替换该字符串。

字符串是字符的集合。

我们可以使用 PHP *str_replace()* 将字符串替换为其他。

**语法**:

```
str_replace(substring,new_replaced_string,original_string);
```

我们需要提供三个参数。

*   su*b 字符串*是原始字符串中存在的应该被替换的字符串
*   *replaced_string* 是替换子串的新字符串。
*   *original_string* 为输入字符串。

**示例 1:** 下面的代码将字符串替换为另一个字符串。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
//input string
$string="Geeks for Geeks";
//replace geeks in the string with computer
echo str_replace("Geeks","computer",$string);
?>
```

**输出:**

```
computer for computer
```

**示例 2:** 以下代码将字符串替换为空。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
//input string
$string="Geeks for Geeks";
//replace geeks in the string with empty
echo str_replace("Geeks","",$string);
?>
```

**输出:**

```
for
```

**示例 3:** 下面的代码将字符串替换为整数。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
//input string
$string="Geeks for Geeks";
//replace geeks in the string with value - 1
echo str_replace("Geeks",1,$string);
?>
```

**输出:**

```
1 for 1
```