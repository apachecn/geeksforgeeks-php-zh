# 在 PHP 中删除字符串末尾出现的特定字符

> 原文:[https://www . geesforgeks . org/从 php 字符串末尾删除特定字符的出现次数/](https://www.geeksforgeeks.org/removing-occurrences-of-a-specific-character-from-end-of-a-string-in-php/)

有很多选项可以删除字符串末尾的所有特定字符。其中一些将在下面讨论:

**[使用 rtrim()函数:](https://www.geeksforgeeks.org/php-rtrim-function/)** 这个函数是 PHP 中的一个内置函数，它从字符串的右侧移除空格或其他字符(如果指定的话)。

**语法:**

```php
rtrim( $string, $charlist )
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **$string:** 是指定要检查的字符串的强制参数。
*   **$charlist:** 是可选参数。它指定要从字符串中删除哪些字符。

**示例:**本示例使用 **rtrim()** 函数移除“.”从最后开始。

```php
<?php

// Declare a variable and initialize it
$string = "GeeksforGeeks is a best platform.....";

// Use rtrim() function to trim
// string from right
echo rtrim($string, ".");

?>
```

**Output:**

```php
GeeksforGeeks is a best platform

```

**[使用 preg_replace()函数:](https://www.geeksforgeeks.org/php-preg_replace-function/)** 该函数是 PHP 中的一个内置函数，用于执行正则表达式来搜索和替换内容。

**语法:**

```php
preg_replace( $patt, $replace, $string, $limit, $count )
```

**参数:**该功能接受五个参数，如上所述，描述如下:

*   **$patt:** 它包含用于搜索内容的字符串元素，可以是字符串或字符串数组。
*   **$replace:** 是指定要替换的字符串或字符串数组的强制参数。
*   **$string:** 要搜索和替换的字符串或字符串数组。
*   **$limit:** 参数指定每个模式的最大可能替换。
*   **$count:** 可选参数。该变量将填充完成的替换次数。

**示例 2:** 本示例使用 **preg_replace()** 功能移除“.”从最后开始。

```php
<?php

// Declare a variable and initialize it
$string = "GeeksforGeeks is a best platform.....";

// Character which need to replace
$regex = "/\.+$/";

// Use preg_replace() function to replace 
// the character
echo preg_replace($regex, "", $string);

?>
```

**Output:**

```php
GeeksforGeeks is a best platform

```