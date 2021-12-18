# PHP openssl_pkey_export()函数

> Original: [https://www.geeksforgeeks.org/php-openssl_pkey_export-function/](https://www.geeksforgeeks.org/php-openssl_pkey_export-function/)

**openssl_pkey_export()**函数是 PHP 中的内置函数，用于查看和管理私钥和公钥。 它将关键字的可导出表示形式导出为字符串。 它将密钥导出为 PEM 编码的字符串，并存储以通过引用传递。

**语法：**

```
*bool* openssl_pkey_export( *mixed* $key, *string* $out [, *string* $passphrase [, *array* $configargs ]])
```

**参数：**此函数接受上述四个参数，如下所述。

*   **$KEY:** this key is passed as an PEM encoded string.
*   **$OUT:** this variable is passed by reference to save the PKCS#12 when the above function is executed successfully.
*   **$password:** this parameter is used to control access to computer systems, programs, or data.
*   The **$configargs:** "configargs" parameter is used to initialize the request. Developers can also mention alternative OpenSSL configuration files by setting the configuration key value to the file path that will be used.

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的程序演示了 PHP 中的**openssl_pkey_export()**函数。

**程序：**

## PHP

```
<?php 

// Create the keypair
$res = openssl_pkey_new();

// Get private key
openssl_pkey_export($res, $privkey, 
                    "PassPhrase number 1"); 
{

    // Get details of public key
    $pubkey = openssl_pkey_get_details($res);
    $pubkey = $pubkey["key"];
    var_dump($privkey);
    var_dump($pubkey);
}

?>  
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.openssl-pkey-export.php](https://www.php.net/manual/en/function.openssl-pkey-export.php)