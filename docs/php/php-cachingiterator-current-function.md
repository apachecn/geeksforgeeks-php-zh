# PHP | CachingIterator current()函数

> 原文:[https://www . geesforgeks . org/PHP-cachingiterator-current-function/](https://www.geeksforgeeks.org/php-cachingiterator-current-function/)

**CachingIterator::current()函数**是 PHP 中的一个内置函数，用来返回当前元素。

**语法:**

```php
*mixed* CachingIterator::current( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数返回 CachingIterator 的当前值。

下面的程序说明了 PHP 中的 CachingIterator::current()函数:

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

// Display the result
foreach($cachIt as $element) {
    echo $cachIt->current() . " ";
}

?>
```

**输出:**

```php
G e e k s

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

// Display the result
foreach($cachIt as $element) {
    echo $cachIt->current() . "\n";
}

?>
```

**输出:**

```php
Geeks
for
Geeks
Computer
Science
Portal

```

**参考:**T2】https://www.php.net/manual/en/cachingiterator.current.php