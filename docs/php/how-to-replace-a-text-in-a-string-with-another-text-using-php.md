# 如何用 PHP 将字符串中的一个文本替换成另一个文本？

> 原文:[https://www . geeksforgeeks . org/如何使用 php 将字符串中的文本替换为另一个文本/](https://www.geeksforgeeks.org/how-to-replace-a-text-in-a-string-with-another-text-using-php/)

一个[字符串](https://www.geeksforgeeks.org/php-strings/)是一个或多个字符的序列。字符串由字符组成，每个字符都可以在脚本中轻松替换。大量[内置的 PHP 方法](https://www.geeksforgeeks.org/php-string-functions/)可以用来执行字符串替换。

**方法 1:使用**[**str _ replace()**](https://www.geeksforgeeks.org/php-str_replace-function/)**方法–****str _ replace()**方法用于将字符串中的文本替换为另一个字符串。但是，该方法会比较上述字符串的大小写。如果没有找到任何匹配的旧字符串，则该字符串保持不变。

```php
str_replace($oldString, $newString, $string)
```

**参数:**

1.  **$oldString:** 指定要搜索和替换的字符串。
2.  **$newString:** 它指定了我们要用$oldString 字符串替换的字符串。
3.  **$string:** 它指定我们要搜索$oldString 并替换为$newString 的字符串或字符串数组。

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Declaring a string variable
$str = "Hi! This is geeksforgeeks";
echo("Original String : ");
echo($str."<br>");

// Old string
$str_old = "This";

// New string
$str_new = "That";

// Replacing part of string
$final_str = str_replace($str_old,$str_new,$str);

echo("Modified String : ");
echo($final_str);

?>
```

**输出:**

```php
Original String : Hi! This is geeksforgeeks
Modified String : Hi! That is geeksforgeeks
```

**注意:**如果在多个部分找到字符串的一部分，则旧字符串的每个实例都会被新的对应字符串替换。下面的代码片段演示了用下划线替换符号“”。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Declaring a string variable
$str = "Hi! This is geeksforgeeks";
echo("Original String : ");
echo($str . "\n");

// Old string
$str_old = " ";

// New string
$str_new = "__";

// Replacing part of string
$final_str = str_ireplace($str_old,$str_new,$str);

echo("Modified String : ");
echo($final_str);

?>
```

**输出:**

```php
Original String : Hi! This is geeksforgeeks
Modified String : Hi!__This__is__geeksforgeeks
```

**方法 2:使用**[**str _ ireplace()**](https://www.geeksforgeeks.org/php-str_ireplace-function/)**方法–**在这种情况下，无论旧字符串处于何种情况下，我们都希望替换字符串，使用 **str_ireplace()** 方法。PHP 5+支持该方法。与 **str_replace()** 方法相比，该字符串的行为方式类似。

**语法:**

```php
str_ireplace($oldString, $newString, $string)
```

**参数:**

*   **$oldString:** 要在字符串中定位的字符串。
*   **$newString:** 替换旧字符串的字符串。
*   **$string:** 指定的字符串。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Declaring a string variable
$str = "Hi! This is geeksforgeeks";

echo("Original String : ");
echo($str . "<br>");

// Old string
$str_old = "GEEKSFoRGEEks";

// New string
$str_new = "GFG";

// Replacing part of string
$final_str = str_ireplace($str_old,$str_new,$str);

echo("Modified String : ");
echo($final_str);

?>
```

**输出:**

```php
Original String : Hi! This is geeksforgeeks
Modified String : Hi! This is GFG
```