# PHP 中最常用的密码哈希方法是什么？

> 原文:[https://www . geesforgeks . org/PHP 中最常用的密码哈希方法是什么/](https://www.geeksforgeeks.org/what-is-the-most-used-method-for-hashing-passwords-in-php/)

哈希密码是一种将单个密码转换为另一个字符串的技术，称为哈希密码。散列密码通常是单向的，即我们不能从散列密码中找到原始密码。所以问题是为什么我们需要使用哈希来做所有这些事情，如果我们可以将密码保存为简单的字符串，为什么还要多走一英里。这样做的唯一原因是为了增强安全性，因为黑客不会从我们有价值的网站上窃取凭据。因此，这就是为什么我们在创建网站和存储数据库时，使用各种哈希方法来哈希密码以保护我们的密码。在 PHP 中，有各种常用的加密算法，如 md5、crypt、sha1 和 bcrypt。现在最常用的是加密散列法。在本文中，我们将学习 PHP 中的加密散列方法。

PHP 提供了一个通用的密码散列函数，用于根据密码创建新的密码散列。

**语法:**

```php
*string* password_hash(*string* $password, *string* $algo, *array* $options = [])
```

这里 **password_hash** 函数主要取三个参数，分别是:

*   **$password:** 您想要散列的密码需要一个字符串值。
*   **$algo:** 您想要用来散列密码的算法。下面是 PHP 中可用的密码算法。
    *   **PASSWORD_BCRYPT:** 它使用 CRYPT_BLOWFISH 算法来创建哈希。
    *   **PASSWORD_ARGON2I:** 使用 ARGON2I 算法进行哈希。
    *   **PASSWORD_ARGON2ID:** 使用 ARGON2ID 算法进行哈希。
    *   **PASSWORD_DEFAULT:** 它使用加密算法进行散列。
*   **$options:** 取盐值默认值为随机盐值。盐值**，**一个额外的字符串，我们在散列时将其附加到字符串中。

**返回值:**返回散列的密码字符串。

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$password = "GeeksforGeeks";
echo "Password is:", $password;

echo "Hashed password using CRYPT_BLOWFISH: ",
    password_hash($password, PASSWORD_BCRYPT);
echo "\n";

echo "Hashed password using Argon2i: ",
    password_hash($password, PASSWORD_ARGON2I);
echo "\n";

echo "Hashed password using bcrypt: ",
    password_hash($password, PASSWORD_DEFAULT);
?>
```

**输出:**

> **密码为:** GeeksforGeeks
> 
> **使用 CRYPT_BLOWFISH 散列的密码:**$ 2y $ 10 $ v4 v4 agaqblwbw 8i/phok9 loptyoxyqze3a z3 cw9 ddvju 7 wxoi
> 
> **使用 Argon2i 进行散列的密码:** $argon2i$v=19$m=65536，t=4，p = 1 $ y2f2tvouvwplyvyucy 9 dsw $ p 164 c 28n 85l 5v 1 i8gis 1 ao 10 zzn M9 e/jayi clax/w
> 
> **使用 bcrypt 散列密码:**2 美元和$10 美元 MQU3vDgoN10。jxyj 1m 9 uqoeqfy . jg 3d 8 tmhdzu akcpgfrwkbblfi

**注意:** 我们没有使用 **PASSWORD_ARGON2ID** ，因为它在标准 PHP 安装中不可用。

**验证散列密码:** PHP 提供了一个名为 password_verify 的内置函数，用于将散列密码与原始密码进行匹配。

**语法:**

```php
*bool* password_verify(*string* $password, *string* $hash)
```

**参数:**

*   **$password:** 我们使用哈希算法哈希的密码。
*   **$hash:** 我们要用原始密码验证的哈希密码。

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$password = "GeeksforGeeks";

$hashed_password =
'$2y$10$MQU3vDgoN10.JxyJ1m9UQOEqFy.Jg3D8tmHdZUAAkcpGFRwkbbLfi';

echo "Original Password is: ", $password;
echo "\n";

echo "Hashed Password is: ", $hashed_password;
echo "\n";

if (password_verify($password, $hashed_password)) {
    echo 'Password is valid!';
} else {
    echo 'Invalid password.';
}

?>
```

**Output**

```php
Original Password is: GeeksforGeeks
Hashed Password is: $2y$10$MQU3vDgoN10.JxyJ1m9UQOEqFy.Jg3D8tmHdZUAAkcpGFRwkbbLfi
Password is valid!
```