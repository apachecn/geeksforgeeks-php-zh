# PHP|utf8_encode()函数

> Original: [https://www.geeksforgeeks.org/php-utf8_encode-function/](https://www.geeksforgeeks.org/php-utf8_encode-function/)

**UTF8_encode()函数**是 PHP 中的一个内置函数，用于将 ISO-8859-1 字符串编码为 UTF-8。 Unicode 被开发来描述所有语言的所有可能的字符，并且包括许多符号，每个符号/字符有一个唯一的数字。 UTF-8 已用于将 Unicode 字符从一台计算机传输到另一台计算机。 将 Unicode 字符可靠地传输到另一台计算机并不总是可行的。

**语法：**

```php
*string* utf8_encode( *string* $string )
```

**参数：**此函数接受必需的单个参数**$string**。 它指定了需要编码的 ISO-8859-1 字符串。

**返回值：**此函数成功时返回表示编码字符串的字符串，失败时返回 False。

**注意：**此函数适用于 PHP 4.0.0 及更新版本。

**示例 1：**

```php
<?php

// String to encode
$string_to_encode = "\x63";

// Encoding string
echo utf8_encode($string_to_encode);

?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```php
<?php

// Creating an array of 256 elements
$text = array(
    "\x20", "\x21", "\x22", "\x23", "\x24", "\x25",
    "\x26", "\x27", "\x28", "\x29", "\x2a", "\x2b",
    "\x2c", "\x2d", "\x2e", "\x2f", "\x30", "\x31", 
    "\x32", "\x33", "\x34", "\x35", "\x36", "\x37", 
);

// Encoding all characters
foreach( $text as $index ) {
    echo utf8_encode($index) . " "; 
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.utf8-encode.php](https://www.php.net/manual/en/function.utf8-encode.php)