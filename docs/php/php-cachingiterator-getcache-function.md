# PHP | CachingIterator getCache()函数

> 原文:[https://www . geesforgeks . org/PHP-cachingiterator-getcache-function/](https://www.geeksforgeeks.org/php-cachingiterator-getcache-function/)

**CachingIterator::getCache()函数**是 PHP 中的一个内置函数，用于检索缓存的内容。

**语法:**

```
*array* CachingIterator::getCache( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数返回包含缓存项目的数组。

下面的程序说明了 PHP 中的 CachingIterator::getCache()函数:

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

// Move to next position
$cachIt->next();

// Display the content of cache
var_dump($cachIt->getCache());

// Move to next position
$cachIt->next();

// Display the content of cache
var_dump($cachIt->getCache());

?>
```

**输出:**

```
array(1) {
  [0]=>
  string(1) "G"
}
array(2) {
  [0]=>
  string(1) "G"
  [1]=>
  string(1) "e"
}

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

// Move to next position
$cachIt->next();
$cachIt->next();
$cachIt->next();

// Display the content of cache
var_dump($cachIt->getCache());

// Move to next position
$cachIt->next();

// Display the content of cache
var_dump($cachIt->getCache());

?>
```

**输出:**

```
array(3) {
  ["a"]=>
  string(5) "Geeks"
  ["b"]=>
  string(3) "for"
  ["c"]=>
  string(5) "Geeks"
}
array(4) {
  ["a"]=>
  string(5) "Geeks"
  ["b"]=>
  string(3) "for"
  ["c"]=>
  string(5) "Geeks"
  ["d"]=>
  string(8) "Computer"
}

```

**参考:**T2】https://www.php.net/manual/en/cachingiterator.getcache.php