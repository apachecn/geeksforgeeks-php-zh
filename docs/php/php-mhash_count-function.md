# PHP mhash_count()函数

> Original: [https://www.geeksforgeeks.org/php-mhash_count-function/](https://www.geeksforgeeks.org/php-mhash_count-function/)

Mhash_count()函数是 PHP 中的一个内置函数，用于获取 SHA1、MD%等系统中安装的当前 MHash 中可用的最高散列 ID。它不接受任何输入参数，并返回一个整数值。

语法：

```php
*int* mhash_count( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个数字索引数组，其中包含支持的散列算法列表。

下面的程序演示了 PHP 中的**mhash_count()**函数：

**程序：**

## PHP

```php
<?php

$nr = mhash_count();

for ($hashNumber = 0; $hashNumber <= $nr; $hashNumber++) {

    // i-th hash name
    $hashName = mhash_get_hash_name($hashNumber);

    // i-th hash block size
    $hashSize = mhash_get_block_size($hashNumber);

   // Details of i-th hash
    echo sprintf("%d Hash is %s and its block size is %d\n", 
                 $hashNumber, $hashName, $hashSize);

}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.mhash-count.php](https://www.php.net/manual/en/function.mhash-count.php)