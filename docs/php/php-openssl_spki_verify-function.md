# PHP openssl_spki_ify()函数

> Original: [https://www.geeksforgeeks.org/php-openssl_spki_verify-function/](https://www.geeksforgeeks.org/php-openssl_spki_verify-function/)

**openssl_spki_ify()**函数是 PHP 中的内置函数，用于验证提供的签名公钥和质询。 这应该是与用于签名的私钥相对应的公钥。 它验证签名的公钥和质询。

**语法：**

```php
*string* openssl_spki_verify( *string* &$spkac )
```

**参数：**此函数接受单个参数，如上所述，如下所述。

*   **$spkac:** the original SPKI only identifies the principal as a public key, but allows binding authorization of these keys and delegation of permissions from one key to another.

**返回值：**此函数在成功或失败时返回布尔值。

**错误/异常：**如果通过**spkac**参数传递无效参数，则 E_WARNING 级别将发出错误。

**示例：**下面的程序演示了 PHP 中的**openssl_spki_ify()**函数。

## PHP

```php
<?php

error_reporting(E_ERROR  | E_PARSE);

/* Array of private key sizes to test */
$ksize = array('1024'=>1024,
               '2048'=>2048,
               '4096'=>4096);

/* Array of available hashings to test */
$algo = array(
    'sha512'=>OPENSSL_ALGO_SHA512,
    'rmd160'=>OPENSSL_ALGO_RMD160
);

/* Loop over key sizes for test */
foreach($ksize as $k => $v) {

    /* generate new private key of 
    specified size to use for tests */
    $pkey = openssl_pkey_new(array
        ('digest_alg' => 'sha512',
        'private_key_type' => OPENSSL_KEYTYPE_RSA,
        'private_key_bits' => $v)
    );

    openssl_pkey_export($pkey, $pass);

    /* Loop to create and verify results */
    foreach($algo as $key => $value) {
        $spkac = openssl_spki_new(
                $pkey, _uuid(), $value);

        echo "Positive verification:: Algo: "
                . $key . ", value:";

        var_dump(openssl_spki_verify(
            preg_replace('/SPKAC=/', '', $spkac)));

        echo "Negative verification:: Algo: "
                . $key . ", value:";
        var_dump(openssl_spki_verify(
                $spkac . 'Make it fail'));
        echo "\n";
    }
    openssl_free_key($pkey);
}

/* Generate a random challenge */
function _uuid() {
    return sprintf(
        '%04x%04x-%04x-%04x-%04x-%04x%04x%04x', 
        mt_rand(0, 0xffff), mt_rand(0, 0xffff), 
        mt_rand(0, 0xffff), mt_rand(0, 0x0fff) | 0x4000,
        mt_rand(0, 0x3fff) | 0x8000, mt_rand(0, 0xffff),
        mt_rand(0, 0xffff), mt_rand(0, 0xffff)
    );
}
?>
```

发帖主题：Re：Колибри0.7.8.0

引用：[https://www.php.net/manual/en/function.openssl-spki-verify.php](https://www.php.net/manual/en/function.openssl-spki-verify.php)