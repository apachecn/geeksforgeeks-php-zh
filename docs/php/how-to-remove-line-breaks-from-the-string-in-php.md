# 如何在 PHP 中删除字符串中的换行符？

> 原文:[https://www . geesforgeks . org/如何从 php 字符串中删除换行符/](https://www.geeksforgeeks.org/how-to-remove-line-breaks-from-the-string-in-php/)

使用 [**str_replace()函数**](https://www.geeksforgeeks.org/php-str_replace-function/) 可以从字符串中删除换行符。str_replace()函数是 PHP 中的一个内置函数，用于用给定字符串或数组中的替换字符串或替换字符串数组分别替换所有出现的搜索字符串或搜索字符串数组。
**语法:**

> str_replace ( $searchVal，$replaceVal，$subjectVal，$count )

**返回类型:**该函数基于带有替换值的$subjectVal 参数返回一个新的字符串或数组。
**示例:**替换< br >标签后，变量文本中采用新字符串。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Declare a variable and initialize it
// with strings containing <br> tag
$text = "Geeks<br>For<br>Geeks";

// Display the string
echo $text;
echo "\n";

// Use str_replace() function to
// remove <br> tag
$text = str_replace("<br>", "", $text);

// Display the new string
echo $text;

?>
```

**Output:** 

```php
Geeks
For
Geeks
GeeksForGeeks
```

**使用** [**preg_replace()函数**](https://www.geeksforgeeks.org/php-preg_replace-function/)**:**preg _ replace()函数是 PHP 中的一个内置函数，用于执行正则表达式来搜索和替换内容。
**语法:**

```php
preg_replace( $pattern, $replacement, $subject, $limit, $count )
```

**返回值:**如果主题参数是数组，则该函数返回一个数组，否则返回一个字符串。
**示例:**本示例使用 preg_replace()函数删除换行符。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Declare a variable and initialize it
// with strings containing <br> tag
$text = "Geeks<br>For<br>Geeks";

// Display the string
echo $text;
echo "\n";

// Use preg_replace() function to
// remove <br> and \n
$text = preg_replace( "/<br>|\n/", "", $text );

// Display the new string
echo $text;

?>
```

**Output:** 

```php
Geeks
For
Geeks
GeeksForGeeks
```