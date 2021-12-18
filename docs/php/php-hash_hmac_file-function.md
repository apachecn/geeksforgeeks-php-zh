# PHP|HASH_HMAC_FILE()函数

> Original: [https://www.geeksforgeeks.org/php-hash_hmac_file-function/](https://www.geeksforgeeks.org/php-hash_hmac_file-function/)

Hash_hmac_file()函数是 PHP 中的一个内置函数，用于使用给定文件的内容生成键控散列值。

**语法：**

```php
*string* hash_hmac_file( $algo, $file, $key, $raw_opt )
```

**参数：**此函数接受上述四个参数，如下所述。

*   **$algo：**它是指定所选散列算法的必需参数。
*   **$file：**此参数用于指定要散列的文件 url。
*   **$key：**此参数用于保存用于生成 HMAC 的共享密钥。
*   **$RAW_OPT：**如果参数设置为 TRUE，则输出将为原始二进制数据，如果参数设置为 FALSE，则输出将为小写十六进制。

**返回值：**此函数以小写十六进制返回包含计算出的消息摘要的字符串。

以下程序使用文件*gfg.txt*，该文件的内容如下：

> GeeksforGeek
> 极客的计算机科学门户

以下程序说明 PHP 中的 HASH_HMAC_FILE()函数：
**程序 1：**

```php
<?php

// PHP program to illustrate
//  hash_hmac_file function

// Create a file to calculate hash of
file_put_contents('gfg.txt', 'Geeks');

// Display result
echo hash_hmac_file('sha1', 'gfg.txt',
            'password', false);
?>
```

发帖主题：Re：Колибри0.7.0

```php
a5365a345a41ac0780bf63e4d33576560b86163c

```

**程序 2：**

```php
<?php

// PHP program to illustrate
//  hash_hmac_file function

// Create a file to calculate hash of
file_put_contents('gfg.txt', 'Geeks');

// Display result
echo hash_hmac_file('sha256', 'gfg.txt', 'password') . "</br>";

// Create a file to calculate hash of
file_put_contents('gfg.txt', 'Content');

// Display result
echo hash_hmac_file('md5', 'gfg.txt', 'password', false);
?>
```

发帖主题：Re：Колибри0.7.0

```php
a73af6923445a30fbacd646622b254069f90c2502e63b1025918aa93f2ddca9d
a7b2b24ac2334070c42a852fb5ef0c92 

```

**引用：**[http://php.net/manual/en/function.hash-file.php](http://php.net/manual/en/function.hash-file.php)