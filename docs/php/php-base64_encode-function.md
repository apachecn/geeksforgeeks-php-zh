# PHP | base64_encode()函数

> 原文:[https://www.geeksforgeeks.org/php-base64_encode-function/](https://www.geeksforgeeks.org/php-base64_encode-function/)

base64_encode()函数是 PHP 中的一个内置函数，用于使用 [MIME base64](https://en.wikipedia.org/wiki/Base64#MIME) 对数据进行编码。MIME(多用途互联网邮件扩展)base64 用于对 base64 中的字符串进行编码。base64 编码数据占用的空间比原始数据多 33%。

**语法:**

```php
string base64_encode( $data )
```

**参数:**该功能接受单参数*$数据*，为必输项。它用于指定字符串编码。

**返回值:**该函数成功时返回 base64 中的编码字符串，失败时返回 False。

下面的程序说明了 PHP 中的 base64_encode()函数:

**程序 1:**

```php
<?php

// Program to illustrate base64_encode()
// function
$str = 'GeeksforGeeks';

echo base64_encode($str);
?>
```

**输出:**

```php
R2Vla3Nmb3JHZWVrcw==

```

**程序二:**

```php
<?php

// Program to illustrate base64_encode()
// function
$str = 'GFG, A computer Science Portal For Geeks';
echo base64_encode($str). "\n";

$str = '';
echo base64_encode($str). "\n";

$str = 1;
echo base64_encode($str). "\n";

$str = '@#{content}apos;;
echo base64_encode($str). "\n";
?>
```

**输出:**

```php
R0ZHLCBBIGNvbXB1dGVyIFNjaWVuY2UgUG9ydGFsIEZvciBHZWVrcw==

MQ==
QCMk

```

**参考:**T2】http://php.net/manual/en/function.base64-encode.php