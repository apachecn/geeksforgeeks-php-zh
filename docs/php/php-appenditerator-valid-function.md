# PHP | AppendIterator 有效()函数

> 原文:[https://www . geesforgeks . org/PHP-appenditerator-valid-function/](https://www.geeksforgeeks.org/php-appenditerator-valid-function/)

**AppendIterator::valid()函数**是 PHP 中的一个内置函数，用于检查当前元素的有效性。

**语法:**

```
*bool* AppendIterator::valid( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**如果当前迭代有效，该函数返回真，否则返回假。

下面的程序说明了 PHP 中的 AppendIterator::valid()函数:

**程序 1:**

```
<?php

// Declare an ArrayIterator
$arr = new ArrayIterator(array('G', 'e', 'e', 'k', 's'));

// Create a new AppendIterator
$itr = new AppendIterator;
$itr->append($arr);

// Check the validity and display
// the result
while($itr->valid()) {
    echo $itr->current();
    $itr->next();
}

?>
```

**输出:**

```
Geeks

```

**程序二:**

```
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

// Check the validity and display the result
while($itr->valid()) { 
    var_dump($itr->current()); 

    // Moving to next element 
    $itr->next(); 
} 

?>
```

**输出:**

```
string(5) "Geeks"
string(3) "for"
string(5) "Geeks"
string(8) "Computer"
string(7) "Science"
string(6) "Portal"

```

**参考:**T2】https://www.php.net/manual/en/appenditerator.valid.php