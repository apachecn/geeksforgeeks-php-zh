# PHP 中如何使用 bcrypt 对密码进行哈希？

> 原文:[https://www . geeksforgeeks . org/如何使用-bcrypt-for-hashing-password-in-PHP/](https://www.geeksforgeeks.org/how-to-use-bcrypt-for-hashing-passwords-in-php/)

每个人都知道并理解，在数据库中以明文形式存储密码是一件相当粗鲁的事情，而且不安全。然而，一些人这样做是因为它使一个网站很容易恢复或测试密码。
bcrypt 是一种用于建立密码安全性的密码哈希技术。它用于保护密码免受黑客攻击，因为密码是以加密格式存储的。

PHP 中的 password_hash()函数是一个内置函数，用于创建新的密码哈希。它使用了一个强大的哈希算法。password_hash()函数与 crypt()函数非常兼容。因此，由 crypt()创建的密码哈希可以与 password_hash()一起使用，反之亦然。函数 password_verify()和 password_hash()只是函数 crypt()的包装器，它们使得准确使用它变得容易得多。

**语法:**

```
*string* password_hash( $password, $algo, $options )
```

password_hash()函数当前支持以下算法:

*   密码 _ 默认值
*   PASSWORD_BCRYPT
*   PASSWORD_ARGON2I
*   PASSWORD_ARGON2ID

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **密码:**存储用户的密码。
*   **algo:** 是连续使用的密码算法常数，同时表示进行密码散列时要使用的算法。
*   **选项:**是一个关联数组，包含选项。如果这被移除并且不包括，将会使用随机盐，并且将会使用默认成本。

**返回值:**成功时返回哈希密码，失败时返回 False。

**示例:**

```
Input : echo password_hash("GFG@123", PASSWORD_DEFAULT);
Output : $2y$10$.vGA19Jh8YrwSJFDodbfoHJIOFH)DfhuofGv3Fykk1a

```

下面的程序说明了 PHP 中的 passwor_hash()函数:

**程序 1:**

```
<?php

echo password_hash("GFG@123", PASSWORD_DEFAULT);
?>
```

**Output:**

```
$2y$10$Z166W1fBdsLcXPVQVfPw/uRq1ueWMA6sLt9bmdUFz9AmOGLdM393G

```

**程序 2:**

```
<?php

$options = [
    'cost' => 12,
];

echo password_hash("GFG@123", PASSWORD_BCRYPT, $options);
?>
```

**Output:**

```
$2y$12$jgzGJmLsUHGNjmDK98MbWe82e3CIJZuflAj6lE1I.dlyhSVfz42oq

```

**程序 3:**

```
<?php

$timeTarget = 0.069; // 69 milliseconds 

$cost = 8;
do {
    $cost++;
    $start = microtime(true);
    password_hash("test", PASSWORD_BCRYPT, ["cost" => $cost]);
    $end = microtime(true);
} while (($end - $start) < $timeTarget);

echo "The appropriate cost is: " . $cost;
?>
```

**Output:**

```
The appropriate cost is: 10

```

**程序 4:**

```
<?php
echo 'Argon2i hash: ' . password_hash('GFG@123', PASSWORD_ARGON2I);
?>
```

**Output:**

```
Argon2i hash: $argon2i$v=19$m=1024,t=2,p=2$YUNvTkJBT2dEejQuUVQvRQ$+96jm/eISqZ7+P9n0DrsBf25piwfnLRy2Yy1VYmb9iI

```

**参考:**T2】https://www.php.net/manual/en/function.password-hash.php