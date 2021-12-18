# PHP|rawurldecode()函数

> Original: [https://www.geeksforgeeks.org/php-rawurldecode-function/](https://www.geeksforgeeks.org/php-rawurldecode-function/)

Rawurldecode()函数是 PHP 中的内置函数，用于解码编码的字符串。 此函数以字符串形式返回解码后的 URL(原始 URL 字符串)。 此函数用文字字符替换后面跟两个十六进制值的%符号。

**语法：**

```php
string rawurldecode( $str )
```

**参数：**此函数接受单个参数*$str*，这是必需的。 它用于存储编码后的 URL。

**返回值：**此函数返回解码 URL 字符串。

下面的程序演示了 PHP 中的 rawurldecode()函数。

**程序 1：**

```php
<?php
    echo rawurldecode("A%20computer%20science%20portal%20for%20geek");
?>
```

**Output:**

```php
A computer science portal for geek

```

**程序 2：**

```php
<?PHP
$str = 'GeeksforGeeks A computer science portal for geek'; 

// Encode the given string
$encode_str = rawurlencode($str); 
echo "Encoded string: " . $encode_str . "<br>";

// Decode the encoded string
$decode_str = rawurldecode($encode_str); 
echo "Decodec string: " . $decode_str;
?>
```

**Output:**

```php
Encoded string: GeeksforGeeks%20A%20computer%20science%20portal%20for%20geek
Decodec string: GeeksforGeeks A computer science portal for geek

```

**相关文章：**

*   [PHP|base64_encode()函数](https://www.geeksforgeeks.org/php-base64_encode-function/)
*   [PHP|base64_decode()函数](https://www.geeksforgeeks.org/php-base64_decode-function/)

**引用：**[http://php.net/manual/en/function.rawurldecode.php](http://php.net/manual/en/function.rawurldecode.php)