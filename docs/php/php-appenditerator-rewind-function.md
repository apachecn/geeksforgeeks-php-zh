# PHP | AppendIterator rewind()函数

> 原文:[https://www . geesforgeks . org/PHP-appenditerator-rewind-function/](https://www.geeksforgeeks.org/php-appenditerator-rewind-function/)

**AppendIterator::rewind()函数**是 PHP 中的一个内置函数，用于回退到第一个内部迭代器的第一个元素。

**语法:**

```php
*void* AppendIterator::rewind( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数不返回值。

下面的程序说明了 PHP 中的 AppendIterator::rewind()函数:

**程序 1:**

```php
<?php

// Declare an ArrayIterator
$arr1 = new ArrayIterator(array("Geeks", "for", "Geeks"));

// Create a new AppendIterator
$itr = new AppendIterator;
$itr->append($arr1);

// Using rewind function 
$itr->rewind(); 

// Get current data  
var_dump($itr->current()); 

// Move on to next object 
$itr->next(); 

// Get current data  
var_dump($itr->current()); 

// Again using rewind function 
$itr->rewind(); 

// Get current data  
var_dump($itr->current()); 

?>
```

**输出:**

```php
string(5) "Geeks"
string(3) "for"
string(5) "Geeks"

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

// Using rewind function 
$itr->rewind(); 

while($itr->valid()) { 
    var_dump($itr->current()); 

    // Moving to next element 
    $itr->next(); 
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

**参考:**T2】https://www.php.net/manual/en/appenditerator.rewind.php