# PHP | CachingIterator getFlags()函数

> 原文:[https://www . geesforgeks . org/PHP-cachingiterator-get flags-function/](https://www.geeksforgeeks.org/php-cachingiterator-getflags-function/)

**CachingIterator::getFlags()函数**是 PHP 中的一个内置函数，用于获取用于此 CachingIterator 实例的标志的位掩码。

**语法:**

```
*int* CachingIterator::getFlags( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**此函数返回用于此 CachingIterator 实例的标志。

下面的程序说明了 PHP 中的 CachingIterator::getFlags()函数:

**程序 1:**

```
<?php

// Declare an array
$arr = array('G', 'e', 'e', 'k', 's');

// Create a new CachingIterator
$cachIt = new CachingIterator(
    new ArrayIterator($arr), 
    CachingIterator::FULL_CACHE
);

// Get the flag
$flag = $cachIt->getFlags();

// Display the flag
var_dump($flag);

?>
```

**输出:**

```
int(256)

```

**程序二:**

```
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

// Get the flag
$flag = $cachIt->getFlags();

// Display the flag value
var_dump($flag);

?>
```

**输出:**

```
int(256)

```

**参考:**T2】https://www.php.net/manual/en/cachingiterator.getflags.php