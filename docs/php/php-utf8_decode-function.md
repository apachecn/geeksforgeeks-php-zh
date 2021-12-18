# PHP|utf8_decode()函数

> Original: [https://www.geeksforgeeks.org/php-utf8_decode-function/](https://www.geeksforgeeks.org/php-utf8_decode-function/)

**UTF8_DECODE()函数**是 PHP 中的内置函数，用于将 UTF-8 字符串解码为 ISO-8859-1。 此函数解码回使用 utf8_encode()函数编码的编码字符串。

**语法：**

```php
*string* utf8_decode( *string* $string )
```

**参数：**此函数接受必需的单个参数**$string**。 它指定要解码的 UTF-8 编码字符串。

**返回值：**此函数成功时返回代表解码字符串的字符串，失败时返回 False。

**注意：**此函数适用于 PHP 4.0.0 及更新版本。

**程序 1：**

## PHP

```php
<?php

// String to decode
$string_to_decode = "\x63";

// Encoding string
echo utf8_encode($string_to_decode) ."<br>";

// Encoding string
echo utf8_decode($string_to_decode);

?>
```

发帖主题：Re：Колибри0.7.0

```php
c
c
```

**程序 2：**

## PHP

```php
<?php

// Creating an array of 256 elements
$text = array(
    "\x20", "\x21", "\x22", "\x23", "\x24", "\x25",
    "\x26", "\x27", "\x28", "\x29", "\x2a", "\x2b",
    "\x2c", "\x2d", "\x2e", "\x2f", "\x30", "\x31"
);

echo "Encoded elements:\n";

// Encoding and decoding all elements
foreach( $text as $index ) {
    echo utf8_encode($index) . " ";
}

echo "\nDecoded elements:\n";

foreach( $text as $index ) {
    echo utf8_decode($index) . " ";
}

?>
```

发帖主题：Re：Колибри0.7.0

```php
Encoded elements:
  ! " # $ % & ' ( ) * + , - . / 0 1 
Decoded elements:
  ! " # $ % & ' ( ) * + , - . / 0 1 
```

**引用：**[https://www.php.net/manual/en/function.utf8-decode.php](https://www.php.net/manual/en/function.utf8-decode.php)