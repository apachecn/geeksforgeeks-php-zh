# 在 PHP 中将逗号分隔的字符串拆分成一个数组

> 原文:[https://www . geeksforgeeks . org/split-a-逗号分隔字符串成数组-in-php/](https://www.geeksforgeeks.org/split-a-comma-delimited-string-into-an-array-in-php/)

给定一个用逗号分隔的长字符串。任务是用逗号分隔符分割给定的字符串，并将结果存储在数组中。

示例:

```php
Input : geeks,for,geeks
Output : Array ( [0] => geeks [1] => for [2] => geeks )

Input : practice, code
Output : Array ( [0] => practice [1] => code )

```

使用 explode()或 preg_split()函数用给定的分隔符在 php 中拆分字符串。

**[PHP | explot()函数](https://www.geeksforgeeks.org/php-explode-function/):**explot()函数是 PHP 中的一个内置函数，用于将一个字符串拆分成不同的字符串。explode()函数根据字符串分隔符拆分字符串，也就是说，它在分隔符出现的地方拆分字符串。此函数返回一个数组，该数组包含通过拆分原始字符串形成的字符串。
<string>语法:</string>

```php
array explode( separator, OriginalString, NoOfElements )
```

**[PHP | preg_split()函数:](https://www.geeksforgeeks.org/php-preg_split-function/)**preg _ split()函数的操作与 split()完全一样，只是正则表达式被接受为模式的输入参数。

**语法:**

```php
array preg_split( string $pattern, string 
$subject [, int $limit = -1 [, int $flags = 0 ]] )
```

**示例:**

```php
<?php

// Use preg_split() function
$string = "123,456,78,000"; 
$str_arr = preg_split ("/\,/", $string); 
print_r($str_arr);

// use of explode
$string = "123,46,78,000";
$str_arr = explode (",", $string); 
print_r($str_arr);
?>
```

**Output:**

```php
Array
(
    [0] => 123
    [1] => 456
    [2] => 78
    [3] => 000
)
Array
(
    [0] => 123
    [1] => 46
    [2] => 78
    [3] => 000
)

```

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。