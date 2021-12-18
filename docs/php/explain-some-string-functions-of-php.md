# 讲解 PHP 的一些字符串函数

> 原文:[https://www . geesforgeks . org/explain-some-string-functions-of-PHP/](https://www.geeksforgeeks.org/explain-some-string-functions-of-php/)

在编程世界中，字符串被认为是一种数据类型，它通常是多个字符的序列，可以包含[空格](https://en.wikipedia.org/wiki/Whitespace_character)、数字、字符以及特殊符号。比如“你好世界！”、“ID-34#90”等。 [PHP](https://www.geeksforgeeks.org/php/) 也允许使用单引号(')来定义字符串。每种编程语言都提供一些内置函数来操作字符串。PHP 提供的一些基本字符串函数如下:

[**strlen()函数**](https://www.geeksforgeeks.org/php-strlen-function/) **:** 它返回字符串的长度，即字符串中所有字符的计数，包括空格字符。

**语法:**

```php
strlen(*string* or *variable* name)
```

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php 

$str = "Hello World!";

// Prints 12 as output
echo strlen($str);

// Prints 13 in a new line
echo "<br>" . strlen("GeeksForGeeks"); 

?>
```

**输出:**

```php
12
13
```

[**【strev()】函数**](https://www.geeksforgeeks.org/php-strrev-function/) **:返回给定字符串的反转字符串。**

**语法:**

```php
strrev(*string or variable name*)
```

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$str = "Hello World!";
echo strrev($str);

?>
```

**Output**

```php
!dlroW olleH
```

[**trim()**](https://www.geeksforgeeks.org/php-trim-function/) **、** [**ltrim()**](https://www.geeksforgeeks.org/php-ltrim-function/) **、**[**rtrim()**](https://www.geeksforgeeks.org/php-rtrim-function/)**，以及**[**chop()**](https://www.geeksforgeeks.org/php-chop-function/)**功能:**它从字符串中删除空格或其他字符。它们有两个参数:一个字符串和另一个 charList，后者是需要省略的字符列表。

*   **修剪()–**从两侧删除字符或空格。
*   **rtrim()**&**chop()–**从右侧移除字符或空格。
*   **ltrim()–**从左侧删除字符或空格。

**注意:**以下示例中给出的代码的浏览器输出可能与这些函数的 HTML 输出不同。

**语法:**

```php
rtrim(*string*, *charList*)
ltrim(*string, charList)*
trim(*string, charList*)
chop(*string, charList*)
```

**参数值:**

*   **$string:** 此强制参数指定要检查的字符串。
*   **$charlist:** 此可选参数指定要从字符串中删除哪些字符。如果未提供此参数，将删除以下字符:
    *   **"\0"** - 空
    *   **" \ t "**–选项卡
    *   **" \ n "**–新线路
    *   **" \ x0B "**–垂直标签
    *   **" \ r "**–回车
    *   **" "**–普通空白

**注意–**参数 *charList* 仅在 PHP 4.1 或更高版本中可用。

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$str = "\nThis is an example for string functions.\n";

// Prints original string
echo $str;

// Removes whitespaces from right end
echo chop($str) . "<br>";

// Removes whitespaces from both ends
echo trim($str) . "<br>";

// Removes whitespaces from right end
echo rtrim($str) . "<br>";

// Removes whitespaces from left end
echo ltrim($str);

?>
```

**Output**

```php
This is an example for string functions.

This is an example for string functions.<br>This is an example for string functions.<br>
This is an example for string functions.<br>This is an example for string functions.

```

[**strtoupper()**](https://www.geeksforgeeks.org/php-strtoupper-function/) **和**[**strto lower()**](https://www.geeksforgeeks.org/php-strtolower-function/)**功能:**其字母换格后返回*字符串*。

*   **strtoupper()–**将所有字母转换为大写后返回字符串。
*   **strtolow()–**将所有字母转换成小写后返回字符串。

**语法:**

```php
strtoupper(*string*)
strtolower(*string*)
```

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$str = "GeeksForGeeks";
echo strtoupper($str)."<br>";
echo strtolower($str);

?>
```

**输出:**

```php
GEEKSFORGEEKS
geeksforgeeks
```

**str_split()函数:**返回一个包含部分字符串的数组。

**语法:**

```php
str_split(*string*, *length*)
```

**参数:**

*   **字符串:**指定要检查的字符串，也可以是类型字符串的变量名。
*   **长度:**指定字符串中要存储的字符串各部分的长度，默认为 1。如果*长度*大于绳子的大小，则返回完整的*绳子*。

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$str = "GeeksForGeeks";
print_r(str_split($str));
echo "<br>";
print_r(str_split($str, 3));

?>
```

**输出:**

```php
Array ( 
    [0] => G 
    [1] => e 
    [2] => e 
    [3] => k 
    [4] => s 
    [5] => F 
    [6] => o 
    [7] => r 
    [8] => G 
    [9] => e 
    [10] => e 
    [11] => k 
    [12] => s 
)
Array ( 
    [0] => Gee 
    [1] => ksF 
    [2] => orG 
    [3] => eek 
    [4] => s 
) 
```