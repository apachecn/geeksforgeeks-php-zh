# PHP | AppendIterator getiterarindex()函数

> 原文:[https://www . geeksforgeeks . org/PHP-appenditerator-getiterarindex-function/](https://www.geeksforgeeks.org/php-appenditerator-getiteratorindex-function/)

**AppendIterator::getiterarindex()函数**是 PHP 中的一个内置函数，用来获取当前内部迭代器的索引。

**语法:**

```php
*int* AppendIterator::getIteratorIndex( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**这个函数返回一个整数值，它是当前内部迭代器的从零开始的索引。

下面的程序说明了 PHP 中的 AppendIterator::getiterarindex()函数:

**程序 1:**

```php
<?php

// Declare an ArrayIterator
$arr1 = new ArrayIterator(array("Geeks", "for", "Geeks"));
$arr2 = new ArrayIterator(array("Computer", "Science", "Portal"));

// Create a new AppendIterator
$itr = new AppendIterator;
$itr->append($arr1);
$itr->append($arr2);

// Display the elements
foreach ($itr as $key => $val) {
    echo "Iterator Index: " . $itr->getIteratorIndex()
        . "  Key : " . $key . "  Value: " . $val . "\n"; 
}

?>
```

**输出:**

```php
Iterator Index: 0  Key : 0  Value: Geeks
Iterator Index: 0  Key : 1  Value: for
Iterator Index: 0  Key : 2  Value: Geeks
Iterator Index: 1  Key : 0  Value: Computer
Iterator Index: 1  Key : 1  Value: Science
Iterator Index: 1  Key : 2  Value: Portal

```

**程序二:**

```php
<?php

// Declare an ArrayIterator
$arr1 = new ArrayIterator(
    array(
        "a" => "Geeks",
        "b" => "for",
        "c" => "Geeks"
    )
);

$arr2 = new ArrayIterator(
    array(
        "x" => "Computer",
        "y" => "Science",
        "z" => "Portal"
    )
);

// Create a new AppendIterator
$itr = new AppendIterator;
$itr->append($arr1);
$itr->append($arr2);

// Display the elements
foreach ($itr as $key => $val) {
    echo "Iterator Index: " . $itr->getIteratorIndex()
        . "  Key : " . $key . "  Value: " . $val . "\n"; 
}

?>
```

**输出:**

```php
Iterator Index: 0  Key : a  Value: Geeks
Iterator Index: 0  Key : b  Value: for
Iterator Index: 0  Key : c  Value: Geeks
Iterator Index: 1  Key : x  Value: Computer
Iterator Index: 1  Key : y  Value: Science
Iterator Index: 1  Key : z  Value: Portal

```

**参考:**[https://www . PHP . net/manual/en/appenditerator . getiterarindex . PHP](https://www.php.net/manual/en/appenditerator.getiteratorindex.php)