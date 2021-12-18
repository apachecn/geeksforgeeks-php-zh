# PHP | AppendIterator append()函数

> 原文:[https://www . geesforgeks . org/PHP-appenditerator-append-function/](https://www.geeksforgeeks.org/php-appenditerator-append-function/)

**AppendIterator::append()函数**是 PHP 中的一个内置函数，用于追加迭代器。

**语法:**

```php
*void* AppendIterator::append( *Iterator* $iterator )
```

**参数:**该函数接受单个参数**$迭代器**，保存要追加的迭代器。

**返回值:**该函数不返回值。

下面的程序说明了 PHP 中的 AppendIterator::append()函数:

**程序 1:**

```php
<?php

// Declare an ArrayIterator
$arr1 = new ArrayIterator(array('G', 'e', 'e', 'k', 's'));
$arr2 = new ArrayIterator(array('f', 'o', 'r'));
$arr3 = new ArrayIterator(array('G', 'e', 'e', 'k', 's'));

// Create a new AppendIterator
$itr = new AppendIterator;
$itr->append($arr1);
$itr->append($arr2);
$itr->append($arr3);

// Display the result
foreach ($itr as $val) {
    echo $val;
}

?>
```

**输出:**

```php
GeeksforGeeks

```

**程序二:**

```php
<?php

// Declare an ArrayIterator
$arr1 = new ArrayIterator(array("Geeks", "for", "Geeks"));
$arr2 = new ArrayIterator(array("Computer", "Science", "Portal"));

// Create a new AppendIterator
$itr = new AppendIterator;
$itr->append($arr1);
$itr->append($arr2);

// Display the result
foreach ($itr as $val) {
    echo $val;
}

?>
```

**输出:**

```php
GeeksforGeeksComputerSciencePortal

```

**参考:**T2】https://www.php.net/manual/en/appenditerator.append.php