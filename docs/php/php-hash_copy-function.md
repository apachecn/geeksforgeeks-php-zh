# PHP|hash_copy()函数

> Original: [https://www.geeksforgeeks.org/php-hash_copy-function/](https://www.geeksforgeeks.org/php-hash_copy-function/)

Hash_copy()函数是 PHP 中的一个内置函数，用于获取散列上下文的副本。

**语法：**

```php
hash_copy( $context )
```

**参数：**此函数接受单个参数*$context*，该参数用于指定 hash_init()函数返回的散列上下文。

**返回值：**此函数返回散列上下文的副本。

下面的程序演示了 PHP 中的 hash_copy()函数：

**程序 1：**

```php
<?php

// Initialize an incremental
// hashing context
$context = hash_init("sha1");

// Copy context using hash_copy function
$cp_context = hash_copy($context);

// Finalize an incremental hash
// and return resulting digest
echo hash_final($context), "\n";

// Update context
hash_update($cp_context, "GFG");

// Print finalize context
echo hash_final($cp_context), "\n";
?>
```

**输出：**

```php
da39a3ee5e6b4b0d3255bfef95601890afd80709
adb536466977c49bebb6317891bffb77dc6e5823

```

**程序 2：**

```php
<?php

// Initialize an incremental
// hashing context
$context = hash_init("md5");

// Copy context using hash_copy function
$cp_context = hash_copy($context);

// Finalize an incremental hash
// and return resulting digest
echo hash_final($context), "\n";

// Update context
hash_update($cp_context, "GFG");

// Print finalize context
echo hash_final($cp_context), "\n";
?>
```

**输出：**

```php
d41d8cd98f00b204e9800998ecf8427e
eadc14b80cd2f247f467eb6c7f45fa9b

```

**引用：**[http://php.net/manual/en/function.hash-copy.php](http://php.net/manual/en/function.hash-copy.php)