# PHP openssl_pkcs12_export_to_file()函数

> Original: [https://www.geeksforgeeks.org/php-openssl_pkcs12_export_to_file-function/](https://www.geeksforgeeks.org/php-openssl_pkcs12_export_to_file-function/)

**openssl_pkcs12_export_to_file()**函数是 PHP 中的内置函数，用于以 PKCS#12 文件格式将 x509 存储到按文件名命名的文件中。 PKCS12 是公钥加密标准，它定义了用于存储服务器证书的存档文件格式。

**语法：**

```php
*bool* openssl_pkcs12_export_to_file( *mixed* $x509, *string* $filename,
        *mixed* $priv_key, *string* $pass [, *array* $args ])
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$x509:** this parameter is the standard for defining the format of public key certificates.
*   **$FILENAME:** this parameter is the path to the output file.
*   **$PRIV_KEY:** this parameter is used for the private key that matches the dessert "PRIV_KEY". The private key is part of the PKCS#12 file.
*   **$PASS:** this parameter is used to unlock the encrypted password of the PKCS#12 file.
*   **$args:** this parameter represents parameters and variables, which are values that represent something else.

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的程序演示了 PHP 中的**openssl_pkcs12_export_to_file()**函数：

**程序：**

## PHP

```php
<?php
$dn = array(
    "countryName" => 'xx',
    "stateOrProvinceName" => 'uttar prradesh',
    "localityName" => 'varanasi',
    "organizationName" => 'geeksforgeeks',
    "organizationalUnitName" => 'geeks team',
    "commonName" => 'people',
    "emailAddress" => 'user@geeks.com'
);

$privateKeyPass = 'abcd1234';
$numberOfDays   = 108;

$privateKey = openssl_pkey_new();
$csr = openssl_csr_new($dn, $privateKey);

// Create a csr file, change null
// to a filename to save
$sscert = openssl_csr_sign($csr, 
    null, $privateKey, $numberOfDays);

// On success $publicKey will 
// hold the PEM content 
openssl_x509_export($sscert, $publicKey);

// Export the privateKey as a PEM content
openssl_pkey_export($privateKey, 
        $privateKey, $privateKeyPass);

$filename = dirname(__FILE__) 
        . '/certificate.pfx';

// Parses the $privateKey and used 
// by openssl_pkcs12_export_to_file
$key = openssl_pkey_get_private(
    $privateKey, $privateKeyPass);

// Save the pfx file to $filename
openssl_pkcs12_export_to_file($sscert, 
    $filename, $key, $privateKeyPass);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.openssl-pkcs12-export-to-file.php](https://www.php.net/manual/en/function.openssl-pkcs12-export-to-file.php)