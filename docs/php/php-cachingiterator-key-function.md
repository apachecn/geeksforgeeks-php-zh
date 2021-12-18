# PHP | CachingIterator 键()函数

> 原文:[https://www . geeksforgeeks . org/PHP-cachingiterator-key-function/](https://www.geeksforgeeks.org/php-cachingiterator-key-function/)

**CachingIterator::key()函数**是 PHP 中的一个内置函数，用于返回当前元素的键。

**语法:**

```
*scalar* CachingIterator::key( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数返回当前元素的键值。

下面的程序说明了 PHP 中的 CachingIterator::key()函数:

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

foreach($cachIt as $element) {
    echo $cachIt->key() . "\n";
}

?>
```

**输出:**

```
0
1
2
3
4

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

foreach($cachIt as $element) {
    echo "key: " . $cachIt->key() . "  Value: "
            . $cachIt->current() . "\n";
}

?>
```

**输出:**

```
key: a  Value: Geeks
key: b  Value: for
key: c  Value: Geeks
key: d  Value: Computer
key: e  Value: Science
key: f  Value: Portal

```

**参考:**T2】https://www.php.net/manual/en/cachingiterator.key.php