# PHP OpenSSL_Verify()函数

> Original: [https://www.geeksforgeeks.org/php-openssl_verify-function/](https://www.geeksforgeeks.org/php-openssl_verify-function/)

**OPENSSL_VERIFY()**函数是 PHP 中的一个内置函数，用于使用与**PUBLIC_KEY**关联的公钥验证**签名**对于指定数据是否正确。 这必须是与用于签名的私钥相对应的公钥。

**语法：**

```php
openssl_verify( $data, $signature, 
    $public_key, $algorithm ): int|false
```

**参数：**此函数接受下面列出的四个参数-

*   **data:** the data string previously used to generate the signature.
*   **signature:** original binary string, generated by openssl_sign () or similar.
*   **PUBLIC_KEY:** key in String-pem format, such as "--BEGIN PUBLIC KEY--MIIBCgK …"
*   **algorithm: a valid string returned by the** openssl_get_md_Methods () function.

**返回值：**如果签名正确，则返回 1；如果签名不正确，则返回 0；如果签名错误，则返回-1 或 false。

**注意：**公钥来自任何支持格式的证书。

下面列出的示例说明了 openssl_ify()函数的用法：

**示例 1：**

## PHP

```php
<?php

// Data you want to sign
$data = 'geeks for geeks';

// Create a new pair of private and public key
$private_key_rsa = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));

$details = openssl_pkey_get_details($private_key_rsa);
$public_key_rsa = openssl_pkey_get_public($details['key']);

// Create signature for your data
openssl_sign($data, $signature, 
    $private_key_rsa, "sha256WithRSAEncryption");

// Verify signature obtained for your data
$result = openssl_verify($data, $signature, 
    $public_key_rsa, OPENSSL_ALGO_SHA256);

if ($result == 1) {
    echo "signature is valid for given data.";
} elseif ($ok == 0) {
    echo "signature is invalid for given data.";
} else {
    echo "error: ".openssl_error_string();
}

?>
```

发帖主题：Re：Колибри0.7.8.0

示例 2：

## PHP

```php
<?php

// Data you want to sign
$data = 'geeks for geeks';

// Create a new pair of private and public key
$private_key_rsa = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));

$details = openssl_pkey_get_details($private_key_rsa);
$public_key_rsa = openssl_pkey_get_public($details['key']);

// Create signature for your data
openssl_sign($data, $signature, 
    $private_key_rsa, "sha256WithRSAEncryption");

// Change the data
$data = 'geeks and geeks';

// Verify signature obtained for your data
$result = openssl_verify($data, $signature, 
    $public_key_rsa, OPENSSL_ALGO_SHA256);

if ($result == 1) {
    echo "signature is valid for given data.";
} elseif ($ok == 0) {
    echo "signature is invalid for given data.";
} else {
    echo "error: ".openssl_error_string();
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.openssl-verify.php](https://www.php.net/manual/en/function.openssl-verify.php)