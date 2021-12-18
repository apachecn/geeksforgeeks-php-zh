# PHP|HASH_HMAC_ALGOS()函数

> Original: [https://www.geeksforgeeks.org/php-hash_hmac_algos-function/](https://www.geeksforgeeks.org/php-hash_hmac_algos-function/)

Hash_hmac_algos()函数是 PHP 中的一个内置函数，用于获取适用于 hash_hmac()函数的已注册散列算法列表。

**语法：**

```
*array* hash_hmac_algos( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含支持的散列算法列表的数组。

下面的程序演示了 PHP 中的 hash_hmac_algos()函数：

**程序：**

```
<?php
print_r(hash_hmac_algos());
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/function.hash-hmac-algos.php](http://php.net/manual/en/function.hash-hmac-algos.php)