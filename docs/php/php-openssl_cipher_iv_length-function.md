# PHP|openssl_cipher_iv_length()函数

> Original: [https://www.geeksforgeeks.org/php-openssl_cipher_iv_length-function/](https://www.geeksforgeeks.org/php-openssl_cipher_iv_length-function/)

**openssl_cipher_iv_length()函数**是 PHP 中的一个内置函数，用于获取密码初始化向量(Iv)的长度。 初始化向量(Iv)是与用于数据加密的秘密密钥一起使用的任意数。 每种密码方法都有一个与其相关联的初始化向量长度。

**语法：**

```php
*int* openssl_cipher_iv_length( *string* $method )
```

**参数：**此函数接受保存密码方法的单个参数**$method**。

**返回值：**此函数成功时返回密码长度，失败时返回 False。

**异常：**当密码算法未知时，此函数引发 E_WARNING 级别错误。

以下示例说明 PHP 中的**openssl_cipher_iv_length()函数**：

**示例 1：**在本程序中，我们将获得 AES-128-GCM 密码算法

```php
<?php

// The cipher method to get iv length of
$method = 'aes-128-gcm';

// Get the iv length
$ivl = openssl_cipher_iv_length($method);

// Output the ivl to
echo $ivl;
?>
```

的 iv 长度

发帖主题：Re：Колибри0.7.8.0

示例 2：在本程序中，我们将获得 Camellia-192-CFB8 密码算法

```php
<?php

// The cipher method to get iv length of
$method = 'camellia-192-cfb8';

// Get the iv length
$ivl = openssl_cipher_iv_length($method);

// Output the ivl to
echo $ivl;
?>
```

的 iv 长度

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.openssl-cipher-iv-length.php](https://www.php.net/manual/en/function.openssl-cipher-iv-length.php)