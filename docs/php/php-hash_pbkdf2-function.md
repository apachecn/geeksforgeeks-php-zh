# PHP|hash_pbkdf2()函数

> Original: [https://www.geeksforgeeks.org/php-hash_pbkdf2-function/](https://www.geeksforgeeks.org/php-hash_pbkdf2-function/)

Hash_pbkdf2()函数是 PHP 中的一个内置函数，用于生成提供的密码的 PBKDF2 密钥派生。

**语法：**

```
*string* hash_pbkdf2( $algo, $pass, $salt, $itr, $len, $raw_opt )
```

**参数：**此函数接受上述六个参数，如下所述。

*   **$algo：**它是指定所选散列算法的必需参数(如-“MD5”、“sha256”、“sha1”)。
*   **$pass：**此参数用于指定用于派生的密码。
*   **$salt：**此参数用于派生，值应随机生成。
*   **$itr：**此参数统计内部迭代的次数。
*   **$len：**此参数用于保存输出字符串的长度。
*   **$RAW_OPT：**如果此参数设置为 True，则其输出将为原始二进制数据，如果此参数设置为 False，则输出将为小写十六进制。

**返回值：**此函数以小写十六进制返回包含计算出的消息摘要的字符串。

以下程序说明了 PHP 中的 hash_pbkdf2()函数：
**程序 1：**

```
<?php
$gfg = "GeeksforGeeks";
$iterations = 142;

// Generate a random IV using 
// openssl_random_pseudo_bytes()
// random_bytes() or another 
// suitable source of randomness.
$salt = openssl_random_pseudo_bytes(16);

// Using hash_pbkdf2 function
$hash = hash_pbkdf2("md5",
    $gfg, $salt, $iterations, 30);

// Display result
echo $hash;
?>
```

**Output:**

```
f0ebbbf59869d76f946c4b15340761

```

**程序 2：**

```
<?php
$gfg = "Contribute1234";
$iterations = 100;

// Generate a random IV using 
// openssl_random_pseudo_bytes()
// random_bytes() or another 
// suitable source of randomness.
$salt = openssl_random_pseudo_bytes(8);

// Using hash_pbkdf2 function
$hash = hash_pbkdf2("md5",
    $gfg, $salt, $iterations, 20, false);

// Display result
echo $hash;
?>
```

**Output:**

```
715b385158045923923c

```

**引用：**[http://php.net/manual/en/function.hash-pbkdf2.php](http://php.net/manual/en/function.hash-pbkdf2.php)