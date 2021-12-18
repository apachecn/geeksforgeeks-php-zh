# 如何在 PHP 中去掉字符串中的所有前导零？

> 原文:[https://www . geeksforgeeks . org/如何删除 php 字符串中的所有前导零/](https://www.geeksforgeeks.org/how-to-remove-all-leading-zeros-in-a-string-in-php/)

给定一个字符串格式的数字，任务是在 PHP 中删除给定字符串的所有前导零。

**例:**

```php
Input : str = 00006665555
Output : 6665555

Input : str = 00775505
Output : 775505

```

**方法 1:使用 [ltrim()函数](https://www.geeksforgeeks.org/php-ltrim-function/):**ltrim()函数用于删除字符串左侧的空格或其他字符(如果指定)。

**语法:**

```php
ltrim( "string", "character which to be remove from the left side of string");
```

**程序:**

```php
<?php

// Store the number string with
// leading zeros into variable
$str = "00775505";

// Passing the string as first
// argument and the character
// to be removed as second
// parameter
$str = ltrim($str, "0"); 

// Display the result
echo $str;

?>
```

**Output:**

```php
775505

```

**方法 2:** 首先将给定的字符串转换为数字，将字符串类型转换为 int，int 将自动删除所有前导零，然后再次将其类型转换为 string，使其再次成为 string。

**程序:**

```php
<?php

// Store the number string with
// leading zeros into variable
$str = "00775505";

// First typecast to int and 
// then to string
$str = (string)((int)($str));

// Display the result
echo $str;

?>
```

**输出:**

```php
775505

```