# PHP openssl_error_string()函数

> Original: [https://www.geeksforgeeks.org/php-openssl_error_string-function/](https://www.geeksforgeeks.org/php-openssl_error_string-function/)

**OPENSSL_ERROR_STRING**()函数是 PHP 中的一个内置函数，用于从 OpenSSL 库中获取最后一个错误。 错误消息已排队，因此应该多次调用此函数来收集所有信息。 最后一个错误将是最近的错误。

**语法：**

```
openssl_error_string(): string|false
```

**参数：**此函数没有参数。

**返回值：**返回错误消息字符串，如果没有其他要返回的错误消息，则返回 False。

下面的示例说明了 PHP 中的 openssl_error_string()函数。

**示例 1：**

## PHP

```
<?php

// Encrypt method to use
$encrypt_method = "AES-256-CBC";

$secret_key = "KEY";

$secret_iv = "KEY";

$string = "geeksforgeeks";

// Generate hash key using sha 256
$key = hash('sha256', $secret_key);

// iv - encrypt method AES-256-CBC
$iv = substr(hash('sha256', $secret_iv) , 0, 16);

// Generate the encrypted text
$output = openssl_encrypt(
      $string, $encrypt_method, $key, 0, $iv);

// Print encrypted output string
echo $output;

echo "\n\n:::: Listed are open ssl "error while encryption:::\n\n";
while ($msg = openssl_error_string()) echo $msg . "\n";

?>
```

发帖主题：Re：Колибри0.7.0

> SXUR6GPO5Kk6WJcS0zuG4A==
> ：列出的是加密时出现的 open ssl 错误：
> 错误：0607A082：数字信封 routines:EVP_CIPHER_CTX_set_key_length:invalid 密钥长度

**示例 2：**

## PHP

```
<?php

// For SSL server certificates the commonName
// is the domain name to be secured
// For S/MIME email certificates the commonName
// is the owner of the email address
// Location and identification fields refer to
// the owner of domain or email subject to be
// secured
$dn = array(
    "countryName" => "IN",
    "stateOrProvinceName" => "Delhi",
    "localityName" => "Delhi",
    "organizationName" => "Geeks for geeks",
    "organizationalUnitName" => "PHP Documentation Team",
    "commonName" => "Geeks",
    "emailAddress" => "wez@example.com"
);

// Generate a new private (and public) key pair
$privkey = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));

// Generate a certificate signing request
$csr = openssl_csr_new($dn, $privkey, array(
    'digest_alg' => 'sha256'
));

// Generate a self-signed cert,
// valid for 365 days
$x509 = openssl_csr_sign($csr,
    null, $privkey, $days = 365, array(
    'digest_alg' => 'sha256'
));

// Save your private key, CSR and 
// self-signed cert for later use
dopenssl_pkey_export($privkey, $pkeyout, "mypassword")
              and var_dump($pkeyout);

// Show any errors that occurred here
while (($e = openssl_error_string()) !== false) {
    echo $e . "\n";
}

?>
```

发帖主题：Re：Колибри0.7.0

> 字符串(1854)“--开始加密私钥--
> 
> MIIFHDBOBgkqhkiG9w0BBQ0wQTApBgkqhkiG9w0BBQwwHAQIPbMk8XYJMNECAggA
> 
> MAwGCCqGSIb3DQIJBQAwFAYIKoZIhvcNAwcECFEhHuj2fzInBIIEyNt/L/HxdXnw
> 
> VJdlJUaG8He7uIa5b8/JVAjd1r5jZqLrSztNG5KipUljGJxYzFTx/eyD6mmVp4
> 
> VrOnOrFyRwHBYQAJyTdEkYQ8J6ogBUdHY724uIIqHcbMo3hKFn0te8xDVWhn0klV
> 
> FdTbhJfGvYlU+HmJRmmR65Ser38CLsSxR55/TUx8PPUY4683VdWS40AIQeCoeVe
> 
> Yn68eN4ylbBWg0N9Zor3D8k8+qmOGTZp3RK69ddavIscEObDtw6iGDbxXa6Q9QC+
> 
> B7/u8wYRBTz0XMLapm4+JFi1F4cQZCFP7pC9VJwiGvfo4hYAT0P3S2eEzCZllF9N
> 
> MFNDjU1AIHpTSD87ZQr‘…
> 
> 错误：0E06D06C：配置文件例程：NCONF_GET_STRING：无值
> 
> 错误：0E06D06C：配置文件例程：NCONF_GET_STRING：无值
> 
> 错误：0E06D06C：配置文件例程：NCONF_GET_STRING：无值
> 
> 错误：0E06D06C：配置文件例程：NCONF_GET_STRING：无值
> 
> 错误：0E06D06C：配置文件例程：NCONF_GET_STRING：无值
> 
> 错误：0E06D06C：配置文件例程：NCONF_GET_STRING：无值
> 
> 错误：0E06D06C：配置文件例程：NCONF_GET_STRING：无值
> 
> 错误：0E06D06C：配置文件例程：NCONF_GET_STRING：无值
> 
> 错误：0E06D06C：配置文件例程：NCONF_GET_STRING：无值
> 
> 错误：0E06D06C：配置文件例程：NCONF_GET_STRING：无值
> 
> 错误：0E06D06C：配置文件例程：NCONF_GET_STRING：无值
> 
> 错误：0E06D06C：配置文件例程：NCONF_GET_STRING：无值
> 
> 错误：0E06D06C：配置文件例程：NCONF_GET_STRING：无值
> 
> 错误：0E06D06C：配置文件例程：NCONF_GET_STRING：无值
> 
> 错误：0E06D06C：配置文件例程：NCONF_GET_STRING：无值

**引用：**[https://www.php.net/manual/en/function.openssl-pkey-export.php](https://www.php.net/manual/en/function.openssl-pkey-export.php)