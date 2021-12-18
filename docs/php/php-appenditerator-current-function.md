# PHP | AppendIterator current()函数

> 原文:[https://www . geesforgeks . org/PHP-appenditerator-current-function/](https://www.geeksforgeeks.org/php-appenditerator-current-function/)

**AppendIterator::current()函数**是 PHP 中的一个内置函数，用来获取当前值。

**语法:**

```php
*mixed* AppendIterator::current( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**如果当前值有效，则返回当前值，否则返回空值。

下面的程序说明了 PHP 中的 AppendIterator::current()函数:

**程序 1:**

```php
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

```php
string(1) "G"
string(1) "e"

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

foreach ($itr as $key => $val) {
    var_dump($itr->current());
}

?>
```

**输出:**

```php
string(5) "Geeks"
string(3) "for"
string(5) "Geeks"
string(8) "Computer"
string(7) "Science"
string(6) "Portal"

```

**参考:**T2】https://www.php.net/manual/en/appenditerator.current.php