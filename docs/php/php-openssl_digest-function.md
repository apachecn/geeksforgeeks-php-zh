# PHP openssl_digest()函数

> Original: [https://www.geeksforgeeks.org/php-openssl_digest-function/](https://www.geeksforgeeks.org/php-openssl_digest-function/)

**openssl_digest()函数**是 PHP 中的内置函数，用于使用给定方法计算给定数据的摘要散列值，并返回原始或二进制十六进制编码的字符串。

**语法：**

```
openssl_digest( string $data, string $digest_algo, 
                   bool $binary = false): string|false
```

**参数：**此函数接受上述四个参数，如下所述-

*   **数据：**要为其创建摘要值的数据。
*   **digest_algo：**要使用的摘要方法，例如“sha256”。
*   **BINARY：**设置为 TRUE 将作为原始输出数据返回，否则返回值为二进制编码。

**返回值：**成功时返回摘要哈希值，失败时返回 False。

下面的程序演示了 PHP 中的 openssl_digest()函数。

**示例 1：**

## PHP

```
<?php

// Data for which digest is to be created
$data = 'geeks for geeks';

// openssl_digest() with sha512 algorithm
// to compute digest value true as
// parameters return the raw input
$fingerPrint = openssl_digest ($data , "sha512", true);

// Print the output of openssl_digest output
print_r($fingerPrint);

?>
```

发帖主题：Re：Колибри0.7.8.0

> O��P�R�：��w�CE�V x�(�eh@\000�7�G�“

**示例 2：**

## PHP

```
<?php

// Data for which digest is to be created
$data = 'geeks for geeks';

// openssl_digest() with sha512 algorithm
// to compute digest value false as 
// parameters return the hex value
$fingerPrint = openssl_digest ($data , "sha512", false);

// Print the output of openssl_digest output
print_r($fingerPrint);

?>
```

发帖主题：Re：Колибри0.7.0

> 6e5f36e9cee5cba6ad938977c98e12f3a61fc4d944753ad130116b026b8ab2c895878910fea3b47dba6d760a20d0b23233980a8dab13f04f262c53f25222b416

**引用：**[https://www.php.net/manual/en/function.openssl-pkey-export.php](https://www.php.net/manual/en/function.openssl-pkey-export.php)