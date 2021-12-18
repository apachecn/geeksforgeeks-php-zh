# PHP openssl_pkcs12_export()函数

> Original: [https://www.geeksforgeeks.org/php-openssl_pkcs12_export-function/](https://www.geeksforgeeks.org/php-openssl_pkcs12_export-function/)

**opensl_pkcs12_export()**函数是 PHP 中的内置函数，用于以 PKCS#12 文件格式存储在名为 x509 的字符串中。 对应于 PKCS#12 变量的证书存储文件。

**语法：**

```
*bool* openssl_pkcs12_export( *mixed* $x509, *string* &$out, 
        *mixed* $priv_key, *string* $pass [, *array* $args] )
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$x509:** this parameter is the standard for defining the format of public key certificates.
*   **$OUT:** this is the variable passed by reference, and the PKCS#12 is saved when the above function is executed successfully.
*   **$PRIV_KEY:** this parameter is used for the private key that matches the dessert "PRIV_KEY". The private key is part of the PKCS#12 file.
*   **$PASS:** this parameter is used to unlock the encrypted password of the PKCS#12 file.
*   **$args:** "$args" represents a parameter, and a variable is a value that represents something else.

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的程序演示了 PHP 中的**openssl_pkcs12_export()**函数：

**程序：**

## PHP

```
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

$privateKeyPass = 'dummyPassword';
$numberOfDays = 108;

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

// Parses the $privateKey and used 
// by openssl_pkcs12_export_to_file.
$key = openssl_pkey_get_private(
    $privateKey, $privateKeyPass);

$certificateOutput = null;

// Save the pfx file to $certificateOutput
openssl_pkcs12_export($sscert, 
    $certificateOutput, $key, $privateKeyPass);

// openssl_pkcs12_read to read the pkcs12
// certificate and store into array
openssl_pkcs12_read ( $certificateOutput, 
    $readableOutput,  $privateKeyPass );

var_dump(($readableOutput));
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.openssl-pkcs12-export.php](https://www.php.net/manual/en/function.openssl-pkcs12-export.php)