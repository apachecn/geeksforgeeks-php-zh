# PHP|hash_algos()函数

> Original: [https://www.geeksforgeeks.org/php-hash_algos-function/](https://www.geeksforgeeks.org/php-hash_algos-function/)

Hash_algos()函数是 PHP 中的一个内置函数，用于返回已注册的散列算法列表。

**语法：**

```php
*array* hash_algos( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个数字索引数组，其中包含支持的散列算法列表。

下面的程序说明了 PHP 中的 hash_algos()函数：
**程序：**

```php
<?php

// hash_algos() function
print_r(hash_algos());
?>
```

**Output:**

```php
Array
(
    [0] => md2
    [1] => md4
    [2] => md5
    [3] => sha1
    [4] => sha224
    [5] => sha256
    [6] => sha384
    [7] => sha512
    [8] => ripemd128
    [9] => ripemd160
    [10] => ripemd256
    [11] => ripemd320
    [12] => whirlpool
    [13] => tiger128,3
    [14] => tiger160,3
    [15] => tiger192,3
    [16] => tiger128,4
    [17] => tiger160,4
    [18] => tiger192,4
    [19] => snefru
    [20] => snefru256
    [21] => gost
    [22] => gost-crypto
    [23] => adler32
    [24] => crc32
    [25] => crc32b
    [26] => fnv132
    [27] => fnv1a32
    [28] => fnv164
    [29] => fnv1a64
    [30] => joaat
    [31] => haval128,3
    [32] => haval160,3
    [33] => haval192,3
    [34] => haval224,3
    [35] => haval256,3
    [36] => haval128,4
    [37] => haval160,4
    [38] => haval192,4
    [39] => haval224,4
    [40] => haval256,4
    [41] => haval128,5
    [42] => haval160,5
    [43] => haval192,5
    [44] => haval224,5
    [45] => haval256,5
)

```

**引用：**[http://php.net/manual/en/function.hash-algos.php](http://php.net/manual/en/function.hash-algos.php)