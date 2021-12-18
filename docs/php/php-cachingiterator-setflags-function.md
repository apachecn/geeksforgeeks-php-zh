# PHP | CachingIterator setFlags()函数

> 原文:[https://www . geesforgeks . org/PHP-cachingiterator-set flags-function/](https://www.geeksforgeeks.org/php-cachingiterator-setflags-function/)

**CachingIterator::setFlags()函数**是 PHP 中的一个内置函数，用于设置 CachingIterator 对象的标志。

**语法:**

```php
*void* CachingIterator::setFlags( *int* $flags )
```

**参数:**该函数接受单个参数 **$flags** ，该参数保存要设置的标志的位掩码值。

**返回值:**该函数不返回值。

下面的程序说明了 PHP 中的 CachingIterator::setFlags()函数:

**程序 1:**

```php
<?php

// Declare an array
$arr = array('G', 'e', 'e', 'k', 's');

// Create a new CachingIterator
$cachIt = new CachingIterator(
    new ArrayIterator($arr), 
    CachingIterator::FULL_CACHE
);

$cachIt->setFlags(128);

// Get the flag
$flag = $cachIt->getFlags();

// Display the flag
var_dump($flag);

?>
```

**输出:**

```php
int(128)

```

**程序二:**

```php
<?php

// Declare an ArrayIterator
$arr = array(
    "a" => "Geeks",
    "b" => "for",
    "c" => "Geeks",
    "d" => "Computer",
    "e" => "Science",
    "f" => "Portal"
);

// Create a new CachingIterator
$cachIt = new CachingIterator(
    new ArrayIterator($arr), 
    CachingIterator::FULL_CACHE
);

// Set the flags
$cachIt->setFlags(512);

// Get the flag
$flag = $cachIt->getFlags();

// Display the flag value
var_dump($flag);

?>
```

**输出:**

```php
int(512)

```

**参考:**T2】https://www.php.net/manual/en/cachingiterator.setflags.php