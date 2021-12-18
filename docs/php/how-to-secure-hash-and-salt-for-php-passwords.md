# 如何保护 PHP 密码的 hash 和 salt？

> 原文:[https://www . geeksforgeeks . org/如何保护 php 密码的哈希和盐/](https://www.geeksforgeeks.org/how-to-secure-hash-and-salt-for-php-passwords/)

盐析和散列是一种将密码存储在数据库中的技术。在密码学中，加盐意味着在密码中加入一些内容，然后对其进行散列。所以盐和散列提供了两个级别的安全性。盐析总是生成唯一的密码，即如果有两个相同的密码，盐析后，生成的字符串将会改变。与散列一起使用的加盐提高了密码的安全级别。

**盐析和散列:**在 PHP 中，通过盐析和散列来存储密码是通过 password_hash()方法完成的。此方法接受三个参数，并返回该密码的最终哈希。

**语法:**

```
*string* password_hash( *string* $pass, *int* $algo, *array* $options )
```

**参数:**

*   **$ pass:** This parameter stores the password to be protected and stored in the database.
*   **$ algo:** It specifies the hash algorithm used to create the $pass hash. Some algorithm parameters in php are:
    1.  [T0】 PASSWORD _ DEFAULT: 【T1] Use bcrypt algorithm (default from PHP 5.5.0). This constant is designed to change over time because new and stronger algorithms are added to PHP.
    2.  [T0】 PASSWORD _ BCRYPT: 【T1] CRYPT_BLOWFISH algorithm is used to create hash. The result is a 60-character string, or FALSE if it fails.
*   **$ option:** is the pickled part. It adopts the form cost factor of salt. It is optional. If left blank, the default cost will be added to the string (10 in most cases). Please note that higher cost will lead to stronger password protection, which will put a heavy load on CPU.

**返回值:**返回哈希密码，失败返回 FALSE。

**示例:**这个示例演示了如何显示 password_hash()，制作 hash 并进行比较。

```
<?php

// Store the string into variable
$password = 'Password';

// Use password_hash() function to
// create a password hash
$hash_default_salt = password_hash($password,
                            PASSWORD_DEFAULT);

$hash_variable_salt = password_hash($password,
        PASSWORD_DEFAULT, array('cost' => 9));

// Use password_verify() function to
// verify the password matches
echo password_verify('Password',
            $hash_default_salt ) . "<br>";

echo password_verify('Password',
            $hash_variable_salt ) . "<br>";

echo password_verify('Password123',
            $hash_default_salt );

?>
```

**输出:**

```
1
1
0

```

在本例中，password_verify()方法用于比较创建的哈希和作为参数输入的字符串。它将哈希和字符串作为参数进行比较，如果密码正确，则返回 true，否则返回 false。