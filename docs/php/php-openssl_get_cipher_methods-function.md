# PHP|openssl_get_cipher_Methods()函数

> Original: [https://www.geeksforgeeks.org/php-openssl_get_cipher_methods-function/](https://www.geeksforgeeks.org/php-openssl_get_cipher_methods-function/)

**openssl_get_cipher_Methods()函数**是 PHP 中的一个内置函数，用于获取所有可用的加密方法。

**语法：**

```
*array* openssl_get_cipher_methods( *bool* $aliases = FALSE )
```

**参数：**此函数接受单个参数**$aliases**，该参数决定是否应该存在密码别名。

**返回值：**此函数返回可用密码方法的数组。

下面给出的程序说明了 PHP 中的**openssl_get_cipher_Methods()函数**：

**程序 1：**在本程序中，我们将列出所有可用的密码。

```
<?php

// Get all the ciphers
$ciphers = openssl_get_cipher_methods();

// Output the cipher to screen
print("<pre>".print_r($ciphers, true)."</pre>");
?>
```

**输出：**

```
Array
(
    [0] => aes-128-cbc
    [1] => aes-128-cbc-hmac-sha1
    [2] => aes-128-cbc-hmac-sha256
    [3] => aes-128-ccm
    [4] => aes-128-cfb
    [5] => aes-128-cfb1
    [6] => aes-128-cfb8
    [7] => aes-128-ctr
     . . . It will be a long list of all the ciphers.
```

**程序 2：**在本程序中，我们将检查是否支持密码。

```
<?php

// Get all the ciphers
$ciphers = openssl_get_cipher_methods();

// Check if aes-128-cfb is supported
$isSupported1 = in_array('aes-128-cfb', $ciphers);

if ($isSupported1) {
    echo 'aes-128-cfb is supported.<br>';
}

// Check if unknown-cipher is supported
$isSupported2 = in_array('unknown-cipher', $ciphers);

if (!$isSupported2) {
    echo 'unknown-cipher is not supported.';
}
?>
```

**输出：**

```
aes-128-cfb is supported.
unknown-cipher is not supported.
```

**引用：**[https://www.php.net/manual/en/function.openssl-get-cipher-methods.php](https://www.php.net/manual/en/function.openssl-get-cipher-methods.php)