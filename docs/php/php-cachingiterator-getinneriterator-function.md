# PHP | CachingIterator getInnerIterator()函数

> 原文:[https://www . geeksforgeeks . org/PHP-cachingiterator-getinneriterator-function/](https://www.geeksforgeeks.org/php-cachingiterator-getinneriterator-function/)

**CachingIterator::getInnerIterator()函数**是 PHP 中的一个内置函数，用于返回发送给构造函数的迭代器。

**语法:**

```
*Iterator* CachingIterator::getInnerIterator( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**这个函数返回一个实现迭代器接口的对象。

下面的程序说明了 PHP 中的 CachingIterator::getinriterator()函数:

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

    echo $element;

    if($cachIt->hasNext()) {
        echo ", ";
    }
}

?>
```

**输出:**

```
G, e, e, k, s

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

    echo $key . " => " . $value;

    if($cachIt->hasNext()) {
        echo "\n";
    }
}

?>
```

**输出:**

```
a => Geeks
b => for
c => Geeks
d => Computer
e => Science
f => Portal

```

**参考:**[https://www . PHP . net/manual/en/cachingiterator . getinneriterator . PHP](https://www.php.net/manual/en/cachingiterator.getinneriterator.php)