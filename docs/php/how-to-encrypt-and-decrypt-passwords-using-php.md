# 如何使用 PHP 对密码进行加密和解密？

> 原文:[https://www . geesforgeks . org/如何使用-php 加密和解密密码/](https://www.geeksforgeeks.org/how-to-encrypt-and-decrypt-passwords-using-php/)

加密和解密密码的最佳方法是在 PHP 中使用标准库，因为从头开始正确加密和解密密码的方法很复杂，并且涉及安全漏洞的多种可能性。使用标准库可以确保哈希实现得到验证和信任。

**注意:**这使用的是 **5.5.0 及以上版本**提供的 **PHP 密码 API** 。

**密码的加密:**要从字符串生成哈希，我们使用 password_hash()函数。

**语法:**

```php
*string* password_hash(string $password, 
          mixed $algo, [array $options])
```

**password_hash()** 函数使用一种可用的哈希算法创建字符串的新密码哈希。它返回当前 60 个字符长的散列，然而，随着新的和更强的算法被添加到 PHP 中，散列的长度可能会增加。因此，建议为可能用于在数据库中存储哈希的列分配 255 个字符。

使用该功能目前支持以下算法:

*   密码 _ 默认值
*   密码 _ 断续器
*   密码 _ 氩气 2i
*   密码 _ 氩气 2id

附加选项可以传递给这个函数，可以用来设置加密的成本，散列过程中使用的盐，等等，在 **$options** 数组中。

以下示例显示了使用 **password_hash()** 方法的方法:

**示例:**

## PHP

```php
<?php

  // The plain text password to be hashed
  $plaintext_password = "Password@123";

  // The hash of the password that
  // can be stored in the database
  $hash = password_hash($plaintext_password, 
          PASSWORD_DEFAULT);

  // Print the generated hash
  echo "Generated hash: ".$hash;
?>
```

**输出:**

> 生成散列:$ 2 & $ 10 $ 7 rlsvrpytqorapkdqmkhtjf 6h9 ljjhng4 hjmsm 2 lhobjbw 5 E6

**密码解密:**要解密密码散列并检索原始字符串，我们使用 **password_verify()** 函数。

**语法:**

```php
*bool* password_verify(string $password, string $hash)
```

**password_verify()** 函数验证由 **password_hash()** 函数生成的给定哈希是否与给定密码匹配。如果密码和哈希匹配，则返回**真**，否则返回**假**。

## PHP

```php
<?php

  // Plaintext password entered by the user
  $plaintext_password = "Password@123";

  // The hashed password retrieved from database
  $hash = 
"$2y$10$8sA2N5Sx/1zMQv2yrTDAaOFlbGWECrrgB68axL.hBb78NhQdyAqWm";

  // Verify the hash against the password entered
  $verify = password_verify($plaintext_password, $hash);

  // Print the result depending if they match
  if ($verify) {
      echo 'Password Verified!';
  } else {
      echo 'Incorrect Password!';
  }
?>
```

**输出:**

```php
Password Verified!
```

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。