# PHP | AppendIterator 键()函数

> 原文:[https://www . geesforgeks . org/PHP-appenditerator-key-function/](https://www.geeksforgeeks.org/php-appenditerator-key-function/)

**AppendIterator::key()函数**是 PHP 中的一个内置函数，用来返回当前键。

**语法:**

```php
*scalar* AppendIterator::key( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**如果当前键有效，则返回当前键，否则返回空。

下面的程序说明了 PHP 中的 AppendIterator::key()函数:

**程序 1:**

```php
<?php

// Declare an ArrayIterator
$arr1 = new ArrayIterator(array('G', 'e', 'e', 'k', 's'));

// Create a new AppendIterator
$itr = new AppendIterator;

// Append the ArrayIterator element
$itr->append($arr1);

// Display the result
while ($itr->valid()) {
    echo "ArrayIterator Key: " . $itr->key() .
    "  ArrayIterator Value: " . $itr->current() . "\n";

    $itr->next();
}

?>
```

**输出:**

```php
ArrayIterator Key: 0  ArrayIterator Value: G
ArrayIterator Key: 1  ArrayIterator Value: e
ArrayIterator Key: 2  ArrayIterator Value: e
ArrayIterator Key: 3  ArrayIterator Value: k
ArrayIterator Key: 4  ArrayIterator Value: s

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

$itr->rewind();

// Display the result
while ($itr->valid()) {
    echo "ArrayIterator Key: " . $itr->key() .
    "  ArrayIterator Value: " . $itr->current() . "\n";

    $itr->next();
}

?>
```

**输出:**

```php
ArrayIterator Key: a  ArrayIterator Value: Geeks
ArrayIterator Key: b  ArrayIterator Value: for
ArrayIterator Key: c  ArrayIterator Value: Geeks
ArrayIterator Key: x  ArrayIterator Value: Computer
ArrayIterator Key: y  ArrayIterator Value: Science
ArrayIterator Key: z  ArrayIterator Value: Portal

```

**参考:**T2】https://www.php.net/manual/en/appenditerator.key.php