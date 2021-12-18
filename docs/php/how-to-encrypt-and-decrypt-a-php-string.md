# 如何加密和解密一个 PHP 字符串？

> 原文:[https://www . geesforgeks . org/如何加密和解密 php 字符串/](https://www.geeksforgeeks.org/how-to-encrypt-and-decrypt-a-php-string/)

在 PHP 中，使用一种称为 OpenSSL 函数的加密扩展来加密和解密字符串是可能的。

**openssl_encrypt()函数:**OpenSSL _ encrypt()函数用于对数据进行加密。

**语法:**

```php
*string* openssl_encrypt( *string* $data, *string* $method, *string* $key,
                        $options = 0, *string* $iv, *string* $tag= NULL,
                        *string* $aad, *int* $tag_length = 16  )

```

**参数:**

*   **$ data:** Save the string or data to be encrypted.
*   **$ method:** The cryptographic method adopts the openssl_get_cipher_methods () function.
*   **$ key:** It holds the encryption key.
*   **$期权:**它保存了 OPENSSL_RAW_DATA 和 OPENSSL_ZERO_PADDING 标志的按位析取。
*   **$ iv:** The initialization vector it saved is not empty.
*   **$ tag:** Save the authentication tag passed by reference when using AEAD cipher mode (GCM or CCM).
*   **$ aad:** Save additional authentication data.
*   **$ tag _ length:** It stores the length of the authentication tag. For GCM mode, the length of authentication label is between 4 and 16.

**返回值:**成功时返回加密字符串，失败时返回 FALSE。

**openssl_decrypt()函数**OpenSSL _ decrypt()函数用于解密数据。

**语法:**

```php
*string* openssl_decrypt( *string* $data, *string* $method, *string* $key,
             *int* $options = 0, *string* $iv, *string* $tag, *string* $aad)

```

**参数:**

*   **$ data:** Save the string or data to be encrypted.
*   **$ method:** The cryptographic method adopts the openssl_get_cipher_methods () function.
*   **$ key:** It holds the encryption key.
*   **$期权:**它保存了 OPENSSL_RAW_DATA 和 OPENSSL_ZERO_PADDING 标志的按位析取。
*   **$ iv:** The initialization vector it saved is not empty.
*   **$ tag:** It uses AEAD password mode (GCM or CCM) to store the authentication tag. Openssl_decrypt () returns FALSE when authentication fails.
*   **$ aad:** Save additional authentication data.

**返回值:**成功时返回解密后的字符串，失败时返回 FALSE。

**方法:**首先声明一个字符串并存储到变量中，使用 openssl_encrypt()函数对给定的字符串进行加密，使用 openssl_decrypt()函数对给定的字符串进行解密。

**例 1:** 这个例子说明了字符串的加密和解密。

```php
<?php

// Store a string into the variable which
// need to be Encrypted
$simple_string = "Welcome to GeeksforGeeks\n";

// Display the original string
echo "Original String: " . $simple_string;

// Store the cipher method
$ciphering = "AES-128-CTR";

// Use OpenSSl Encryption method
$iv_length = openssl_cipher_iv_length($ciphering);
$options = 0;

// Non-NULL Initialization Vector for encryption
$encryption_iv = '1234567891011121';

// Store the encryption key
$encryption_key = "GeeksforGeeks";

// Use openssl_encrypt() function to encrypt the data
$encryption = openssl_encrypt($simple_string, $ciphering,
            $encryption_key, $options, $encryption_iv);

// Display the encrypted string
echo "Encrypted String: " . $encryption . "\n";

// Non-NULL Initialization Vector for decryption
$decryption_iv = '1234567891011121';

// Store the decryption key
$decryption_key = "GeeksforGeeks";

// Use openssl_decrypt() function to decrypt the data
$decryption=openssl_decrypt ($encryption, $ciphering, 
        $decryption_key, $options, $decryption_iv);

// Display the decrypted string
echo "Decrypted String: " . $decryption;

?>
```

**输出:**

```php
Original String: Welcome to GeeksforGeeks
Encrypted String: hwB1K5NkfcIzkLTWQeQfHLNg5FlyX3PNUA==
Decrypted String: Welcome to GeeksforGeeks

```

**示例 2:** 下面的示例说明了字符串的加密和解密。这里要加密的字符串和解密的字符串将是相同的，但加密的字符串是随机变化的。

```php
<?php

// Store a string into the variable which
// need to be Encrypted
$simple_string = "Welcome to GeeksforGeeks";

// Display the original string
echo "Original String: " . $simple_string . "\n";

// Store cipher method
$ciphering = "BF-CBC";

// Use OpenSSl encryption method
$iv_length = openssl_cipher_iv_length($ciphering);
$options = 0;

// Use random_bytes() function which gives
// randomly 16 digit values
$encryption_iv = random_bytes($iv_length);

// Alternatively, we can use any 16 digit
// characters or numeric for iv
$encryption_key = openssl_digest(php_uname(), 'MD5', TRUE);

// Encryption of string process starts
$encryption = openssl_encrypt($simple_string, $ciphering,
        $encryption_key, $options, $encryption_iv);

// Display the encrypted string
echo "Encrypted String: " . $encryption . "\n";

// Decryption of string process starts
// Used random_bytes() which gives randomly
// 16 digit values
$decryption_iv = random_bytes($iv_length);

// Store the decryption key
$decryption_key = openssl_digest(php_uname(), 'MD5', TRUE);

// Descrypt the string
$decryption = openssl_decrypt ($encryption, $ciphering,
            $decryption_key, $options, $encryption_iv);

// Display the decrypted string
echo "Decrypted String: " . $decryption;

?>
```

**输出:**

```php
Original String: Welcome to GeeksforGeeks
Encrypted String: hwB1K5NkfcIzkLTWQeQfHLNg5FlyX3PNUA==
Decrypted String: Welcome to GeeksforGeeks

```

**参考文献:**

*   [【https://www . PHP . net/manual/en/function . OpenSSL-encrypt . PHP】](https://www.php.net/manual/en/function.openssl-encrypt.php)
*   [https://www.php.net/manual/en/function.openssl-decrypt.php](https://www.php.net/manual/en/function.openssl-decrypt.php)

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。