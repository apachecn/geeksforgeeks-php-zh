# PHP openssl_spki_export_challengl()函数

> Original: [https://www.geeksforgeeks.org/php-openssl_spki_export_challenge-function/](https://www.geeksforgeeks.org/php-openssl_spki_export_challenge-function/)

**openssl_spki_export_challengl()**函数是 PHP 中的内置函数，用于导出签名的公钥和与之相关的质询。 它验证签名的公钥和质询。

**语法：**

```
*string* openssl_spki_export_challenge( *string* &$spkac )
```

**参数：**此函数接受如上所述的单个参数：

*   **$spkac:** this parameter is a format for sending a certificate signing request that encodes a public key that can be operated using **openssl** .

**返回值：**此函数在失败时返回关联的质询字符串或 NULL。

**错误/异常：**如果使用“spkac”参数传递无效参数，则 E_WARNING 级别将发出错误。

下面的程序演示了 PHP 中的**openssl_spki_export_challengl()**函数：

**程序：**

## PHP

```
<?php

$pkey   = openssl_pkey_new(array("spki"));
$inputChallengeString = "geeks";

// Generate a new key pair using 
// "geeksforgeeks" as challenge string
$spkac = openssl_spki_new(
        $pkey, $inputChallengeString);

// Extract challenge key from key
$extractedChallengeString = 
    openssl_spki_export_challenge(
    preg_replace('/SPKAC=/', '', $spkac));

//if challenge string is not null
if (! is_null($extractedChallengeString)) {
    echo "Used challenge string is:" 
        . $inputChallengeString."\n";

    // print challenge key
    echo "Extracted challenge string is:"
        . $extractedChallengeString . "\n";
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.openssl-spki-export-challenge.php](https://www.php.net/manual/en/function.openssl-spki-export-challenge.php)