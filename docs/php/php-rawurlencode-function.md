# PHP|rawurlencode()函数

> Original: [https://www.geeksforgeeks.org/php-rawurlencode-function/](https://www.geeksforgeeks.org/php-rawurlencode-function/)

Rawurlencode()函数是 PHP 中的一个内置函数，用于根据[RFC(统一资源标识符)3986](http://www.faqs.org/rfcs/rfc3986.html)对 URL(统一资源定位符)进行编码。

**语法：**

```
string rawurlencode( $str )
```

**参数：**此函数接受单个参数*$str*，这是必需的。 用于存储要编码的 URL。

**返回值：**此函数返回一个字符串，该字符串包含除-_.~符号之外的所有非字母数字字符。 符号或空格字符替换为百分号(%)，后跟两个十六进制数字。

下面的程序演示了 PHP 中的 rawurlencode()函数。

**程序 1：**

```
<?php
echo '<a href="www.geeksforgeeks.org',
  rawurlencode('A computer science portal for geek'), '">';
?>
```

**输出：**

```
<a href="www.geeksforgeeks.orgA%20computer%20science%20portal%20for%20geek">

```

**程序 2：**

```
<?php

// Store the URL string
$str = 'A computer science portal for geek';

// Encode the URL string and print it.
echo '<a href="www.geeksforgeeks.org', rawurlencode($str), '">';
?>
```

**输出：**

```
<a href="www.geeksforgeeks.orgA%20computer%20science%20portal%20for%20geek">

```

**相关文章：**

*   [php|base64_encode()函数](https://www.geeksforgeeks.org/php-base64_encode-function/)
*   [php|base64_decode()函数](https://www.geeksforgeeks.org/php-base64_decode-function/)

**引用：**[http://php.net/manual/en/function.rawurlencode.php](http://php.net/manual/en/function.rawurlencode.php)