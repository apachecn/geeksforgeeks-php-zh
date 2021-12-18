# 如何在 PHP 中获取字符串中字符的位置？

> 原文:[https://www . geesforgeks . org/如何获取 php 字符串中字符的位置/](https://www.geeksforgeeks.org/how-to-get-the-position-of-character-in-a-string-in-php/)

在本文中，我们将获得 PHP 中给定字符串中字符的位置。字符串是一组字符。我们将通过使用[**<u>【strpos()</u>函数**](https://www.geeksforgeeks.org/php-strpos-stripos-functions/) 来获取字符串中字符的位置。

**语法:**

```php
strpos(string, character, start_pos)
```

**参数:**

*   **字符串(必选):**这个参数是指我们需要在其中搜索所需字符串出现的原始字符串。
*   **字符(必选):**这个参数是指我们需要搜索的字符串。
*   **start_pos(可选):**指搜索必须开始的字符串位置。

**返回值:**返回字符的索引位置。

**示例 1:** 获取给定字符串中特定字符位置的 PHP 程序。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Consider the string
$str1 = "Hello geeks for geeks";

// Get the position of 'f' character
echo strpos($str1, 'f');
echo "\n";

// Get the position of 'H' character
echo strpos($str1, 'H');
echo "\n";

// Get the position of 'l' character
echo strpos($str1, 'l');
echo "\n";

// Get the position of ' ' space  
echo strpos($str1, ' ');

?>
```

**Output**

```php
12
0
2
5
```

**例 2:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Consider the string
$str1 = "Hello geeks for geeks";

// Get the position of 'f' character
// starts from 5th index
echo strpos($str1, 'f', 5);
echo "\n";

// Get the position of 'H' character
// starts from 8th index
// No output since H is present at 1st
// position, we started from 8th position 
echo strpos($str1, 'H', 8);

?>
```

**Output**

```php
12

```