# PHP | CachingIterator rewind()函数

> 原文:[https://www . geesforgeks . org/PHP-cachingiterator-rewind-function/](https://www.geeksforgeeks.org/php-cachingiterator-rewind-function/)

**CachingIterator::rewind()函数**是 PHP 中的一个内置函数，用来倒带迭代器。

**语法:**

```php
*void* CachingIterator::rewind( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数不返回值。

下面的程序说明了 PHP 中的 CachingIterator::rewind()函数:

**程序 1:**

```php
<?php 

// Declare an ArrayIterator 
$arr = new ArrayIterator( 
    array( 
        "a" => 4, 
        "b" => 2, 
        "g" => 8, 
        "d" => 6, 
        "e" => 1, 
        "f" => 9 
    ) 
); 

// Create a new CachingIterator
$cachIt = new CachingIterator(
    new ArrayIterator($arr), 
    CachingIterator::FULL_CACHE
);

// Move to last position 
$cachIt->seek(5); 

// Display the next value 
var_dump($cachIt->next()); 

// Move to start position 
$cachIt->rewind(); 

// Display the current element 
echo $cachIt->current(); 

?>
```

**输出:**

```php
NULL
4

```

**程序二:**

```php
<?php 

// Declare an ArrayIterator 
$arr = new ArrayIterator( 
    array( 
        "b" => "for", 
        "a" => "Geeks", 
        "e" => "Science", 
        "c" => "Geeks", 
        "f" => "Portal", 
        "d" => "Computer"
    ) 
); 

// Create a new CachingIterator
$cachIt = new CachingIterator(
    new ArrayIterator($arr), 
    CachingIterator::FULL_CACHE
);

// Check the validity of ArrayIterator 
while($cachIt->valid()) { 
    $cachIt->next(); 
} 

// Move to start position 
$cachIt->rewind(); 

// Display the current element 
echo $cachIt->current(); 

?>
```

**输出:**

```php
for

```

**参考:**T2】https://www.php.net/manual/en/cachingiterator.rewind.php