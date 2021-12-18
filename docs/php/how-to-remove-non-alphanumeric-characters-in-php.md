# PHP 中如何去掉非字母数字字符？

> 原文:[https://www . geesforgeks . org/如何删除非字母数字字符 php/](https://www.geeksforgeeks.org/how-to-remove-non-alphanumeric-characters-in-php/)

使用 preg_replace()函数可以删除非字母数字字符。该函数执行正则表达式搜索和替换。函数 preg_replace()搜索由模式指定的字符串，如果找到，用替换替换模式。

示例:

```php
Input : !@GeeksforGeeks2018?
Output : GeeksforGeeks2018

Input : Geeks For Geeks
Output : GeeksForGeeks

```

**语法:**

```php
*int* preg_match( $pattern, $replacement_string, $original_string )
```

**参数:**该函数接受三个参数，如上所述，如下所述:

*   **$pattern:** 在字符串中搜索的模式。它必须是正则表达式。
*   **$replacement_string:** 匹配的模式被 replacement_string 替换。
*   **$original_string:** 是进行搜索替换的原始字符串。

**返回值:**

*   替换发生后，将返回修改后的字符串。
*   如果没有找到匹配项，原始字符串保持不变。

**方法 1:** 正则表达式*/[\ W]/'*匹配所有非字母数字字符，并用' '(空字符串)替换。

```php
$str = preg_replace( '/[\W]/', '', $str);
```

在正则表达式中，W 是一个元字符，前面有一个反斜杠(\W)，它赋予组合特殊的含义。它表示非字母数字字符的组合。

**示例:**

```php
<?php 

// string containing non-alphanumeric characters
$str="!@GeeksforGeeks2018?";

// preg_replace function to remove the
// non-alphanumeric characters
$str = preg_replace( '/[\W]/', '', $str);

// print the string
echo($str);
?>
```

**Output:**

```php
GeeksforGeeks2018

```

**方法 2:** 正则表达式*'/[^a-z0-9/I '*匹配所有非字母数字字符，并用' '(空字符串)替换它们。

```php
$str = preg_replace( '/[^a-z0-9 ]/i', '', $str);
```

在正则表达式中:

*   **i:** 用于不区分大小写。
*   **a-z:** 用于所有小写字母，不需要指定 a-z，因为 I(不区分大小写)已经在语句中提到了。
*   **0-9:** 用于匹配所有数字。

**示例:**

```php
<?php 

// string containing non-alphanumeric characters
$str="!@GeeksforGeeks2018?";

// preg_replace function to remove the 
// non-alphanumeric characters
$str = preg_replace( '/[^a-z0-9]/i', '', $str);

// print the string
echo($str);
?>
```

**Output:**

```php
GeeksforGeeks2018

```