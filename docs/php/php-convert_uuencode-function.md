# PHP | convert_uuencode()函数

> 原文:[https://www . geesforgeks . org/PHP-convert _ uuencode-function/](https://www.geeksforgeeks.org/php-convert_uuencode-function/)

*convert_uuencode()* 是 PHP 中的内置函数。convert_uuencode()函数使用 [uuencode 算法](https://en.wikipedia.org/wiki/Uuencoding)对字符串进行编码。
Uuencode 编码将所有字符串(包括二进制数据)转换为可打印字符，这使得它们对于网络传输是安全的。

**语法:**

```php
*String* convert_uuencode($string)

```

**参数:**该函数接受单个参数 *$string* ，该参数是解编码所需的字符串。

**返回值:**这个函数返回一个代表未编码数据的字符串。

**示例:**

```php
Input : "Good Morning..."
Output : /1V]O9"!-;W)N:6YG+BXN
`

Input : "I love my india"
Output : /22!L;W9E(&UY(&EN9&EA`

```

下面的程序说明了 convert_uuencode()函数:

```php
<?php

// PHP program illustrate the 
// convert_uuencode() function

// Input String
$str = "geeks for geeks!";

// Encoding the string
$encodeString = convert_uuencode($str);

// printing encoded string
echo $encodeString . "\n";

// Decode the string
$decodeString = convert_uudecode($encodeString);
echo $decodeString;

?> 
```

输出:

```php
09V5E:W, @9F]R(&=E96MS(0``
geeks for geeks! 

```

**参考**:
T3】http://php.net/manual/en/function.convert-uuencode.php