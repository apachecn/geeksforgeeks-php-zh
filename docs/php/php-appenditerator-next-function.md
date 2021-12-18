# PHP | AppendIterator next()函数

> 原文:[https://www . geesforgeks . org/PHP-appenditerator-next-function/](https://www.geeksforgeeks.org/php-appenditerator-next-function/)

**AppendIterator::next()函数**是 PHP 中的一个内置函数，用于将元素移动到下一个元素中。

**语法:**

```
*void* AppendIterator::next( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数不返回值。

下面的程序说明了 PHP 中的 AppendIterator::next()函数:

**程序 1:**

```
<?php

// Declare an ArrayIterator
$arr1 = new ArrayIterator(array('G', 'e', 'e', 'k', 's'));

// Create a new AppendIterator
$itr = new AppendIterator;

// Append the ArrayIterator element
$itr->append($arr1);

// Display the current element of iterator
var_dump($itr->current());

// Use AppendIterator::next() function to
// move into next element
$itr->next();

// Display the current element of iterator
var_dump($itr->current());

?>
```

**输出:**

```
string(1) "G"
string(1) "e"

```

**程序二:**

```
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

$itr->rewind();

while ($itr->valid()) {
    echo "ArrayIterator Key: " . $itr->key() .
    "  ArrayIterator Value: " . $itr->current() . "\n";

    $itr->next();
}

?>
```

**输出:**

```
ArrayIterator Key: a  ArrayIterator Value: Geeks
ArrayIterator Key: b  ArrayIterator Value: for
ArrayIterator Key: c  ArrayIterator Value: Geeks
ArrayIterator Key: x  ArrayIterator Value: Computer
ArrayIterator Key: y  ArrayIterator Value: Science
ArrayIterator Key: z  ArrayIterator Value: Portal

```

**参考:**T2】https://www.php.net/manual/en/appenditerator.next.php