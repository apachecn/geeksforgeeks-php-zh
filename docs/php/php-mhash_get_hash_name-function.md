# PHP mhash_get_hash_name()函数

> Original: [https://www.geeksforgeeks.org/php-mhash_get_hash_name-function/](https://www.geeksforgeeks.org/php-mhash_get_hash_name-function/)

**mhash_get_hash_name()**函数是 PHP 中的内置函数，用于获取指定散列的块大小。 它获取系统中安装的当前 MHash 中可用的最高散列 ID，如 SHA1、MD%等。

**语法：**

```php
*string* mhash_get_hash_name( *int* $hash )
```

**参数：**如下所述，此函数接受单个参数：

*   **$Hash:** this is the hash ID. One of the *mhash_name* constants.

**返回值：**此函数仅返回包含支持的哈希算法列表的哈希名。

**示例：**下面的示例说明了 PHP 中的**mhash_get_hash_name()**函数。

## PHP

```php
<?php

$maxHashCount = mhash_count();

for ($hashNumber = 0; $hashNumber 
  <= $maxHashCount; $hashNumber++) {

    // i-th hash name
    $hashName = mhash_get_hash_name($hashNumber);

    // i-th block size
    print_r($hashName."\n");        
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.mhash-get-hash-name.php](https://www.php.net/manual/en/function.mhash-get-hash-name.php)