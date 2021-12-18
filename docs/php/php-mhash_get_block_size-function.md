# PHP mhash_get_block_size()函数

> Original: [https://www.geeksforgeeks.org/php-mhash_get_block_size-function/](https://www.geeksforgeeks.org/php-mhash_get_block_size-function/)

**mhash_get_block_size()**函数是 PHP 中的内置函数，用于获取指定散列的块大小。 获取系统中安装的当前 MHash 中可用的最高哈希 ID，如 SHA1、MD%等。

**语法：**

```php
int mhash_get_block_size( int $hash )
```

**参数：**此函数接受一个参数，如上面的语法所示。 参数描述如下：

*   **$Hash:** Hash ID. One of the MHASH_HASHNAME constants.

**返回值：**此函数返回散列名及其块大小，其中包含支持的散列算法列表。

示例：下面的程序演示了 PHP 中的**mhash_get_block_size()**函数。

## PHP

```php
<?php

$maxHashCount = mhash_count();

for ($hashNumber = 0; $hashNumber <= 
        $maxHashCount; $hashNumber++) {

    // i-th hash name
    $hashName = mhash_get_hash_name($hashNumber);

    // i-th block size
    $hashSize = mhash_get_block_size($hashNumber);

    // Details of i-th hash
    print_r($hashName . " 's block size is" 
                . $hashSize . "\n");
}
?>
```

发帖主题：Re：Колибри0.7.8.0