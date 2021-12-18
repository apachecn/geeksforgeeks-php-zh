# PHP mhash_keygen_s2k()函数

> Original: [https://www.geeksforgeeks.org/php-mhash_keygen_s2k-function/](https://www.geeksforgeeks.org/php-mhash_keygen_s2k-function/)

**mhash_keygen_s2k()**函数是 PHP 中的内置函数，用于使用用户提供的密码根据给定的散列生成密钥。 这是 OpenPGP 文档(RFC 2440)中指定的加盐 S2K 算法。 此函数可用于计算校验和、消息摘要等。
Salt 是用于生成密钥的随机数据片段。 要检查钥匙，你还必须知道盐，所以最好也加上盐。

**语法：**

```php

*string* mhash_keygen_s2k(*int* $hash, *string* $password, 
                *string* $salt, *int* $bytes)
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$Hash：**此参数保存散列 ID，即**mhash_name**常量之一。
*   **$password：**此参数保存用户的密码。
*   **$Salt：**盐是随机数据，用作单向函数的附加输入，该函数对数据、密码或口令进行散列。 SALT 的固定长度为 8 个字节，如果您提供的字节较少，则将用零填充。
*   **$Bytes：**此参数以字节为单位表示密钥长度。

**返回值：**此函数以字符串形式返回生成的键，如果出错则返回 False。

下面的程序演示了 PHP 中的**mhash_keygen_s2k()**函数：

**程序：**

## PHP

```php
<?php

$inputString  = "p4ssw0rd" ;
$salt = "agejkhgeuka";

$bytes = "8";

// bin2hex is used to convert binary
// to hex string

print_r(bin2hex(mhash_keygen_s2k(
      MHASH_MD5, $inputString, $salt, $bytes)));

?>
```

发帖主题：Re：Колибри0.7.0

```php
e2dfb845290aae21
```