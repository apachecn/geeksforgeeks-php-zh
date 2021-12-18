# PHP | CachingIterator next()函数

> 原文:[https://www . geeksforgeeks . org/PHP-cachingiterator-next-function/](https://www.geeksforgeeks.org/php-cachingiterator-next-function/)

**CachingIterator::next()函数**是 PHP 中的一个内置函数，用于向前移动迭代器。

**语法:**

```
*void* CachingIterator::next( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数不返回值。

下面的程序说明了 PHP 中的 CachingIterator::next()函数:

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
    echo $cachIt->current() . " ";
    $cachIt->next();
}

?>
```

**输出:**

```
G e s

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

foreach($cachIt as $key => $value) {
    echo $key . " => " . $cachIt->current() . "\n";
    $cachIt->next();
}

?>
```

**输出:**

```
a => Geeks
c => Geeks
e => Science

```

**参考:**T2】https://www.php.net/manual/en/cachingiterator.next.php