# PHP | base64_decode()函数

> 原文:[https://www.geeksforgeeks.org/php-base64_decode-function/](https://www.geeksforgeeks.org/php-base64_decode-function/)

base64_decode()是 PHP 中的一个内置函数，用于解码以 MIME base64 编码的数据。
**语法:**

```
*string* base64_decode( $data, $strict )
```

**参数:**该功能接受两个参数，如上所述，描述如下:

*   **$data:** 包含编码字符串的强制参数。
*   **$strict:** 是可选参数。如果此参数设置为真，那么如果输入包含 base64 字母表之外的字符，base64_decode()函数将返回假。无效字符将被默默丢弃。

**返回值:**该函数成功时返回解码后的字符串，失败时返回 False。
下面的程序说明了 PHP 中的 base64_decode()函数:
**程序 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Program to illustrate base64_decode()
// function
$str = 'R2Vla3Nmb3JHZWVrcw==';

echo base64_decode($str);
?>
```

**Output:** 

```
GeeksforGeeks
```

**节目 2:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Program to illustrate base64_decode()
// function
$str = 'R0ZHLCBBIGNvbXB1dGVyIFNjaWVuY2UgUG9ydGFsIEZvciBHZWVrcw';
echo base64_decode($str). "\n";

$str = 'MQ==';
echo base64_decode($str). "\n";
?>
```

**Output:** 

```
GFG, A computer Science Portal For Geeks
1
```

**参考:**T2http://php.net/manual/en/function.base64-decode.php