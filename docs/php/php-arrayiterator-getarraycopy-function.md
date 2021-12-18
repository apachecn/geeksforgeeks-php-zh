# PHP | ArrayIterator getArrayCopy()函数

> 原文:[https://www . geeksforgeeks . org/PHP-arrayiterator-getarraycopy-function/](https://www.geeksforgeeks.org/php-arrayiterator-getarraycopy-function/)

**ArrayIterator::getArrayCopy()函数**是 PHP 中的一个内置函数，用于创建数组的副本。

**语法:**

```php
*array* ArrayIterator::getArrayCopy( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数返回数组的副本。

下面的程序说明了 PHP 中的 ArrayIterator::getArrayCopy()函数:

**程序 1:**

```php
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array('G', 'e', 'e', 'k', 's', 'f', 'o', 'r')
);

// Create a copy of array
$copyArr = $arrItr->getArrayCopy();

// Display the array iterator element
var_dump($copyArr);

?>
```

**输出:**

```php
array(8) {
  [0]=>
  string(1) "G"
  [1]=>
  string(1) "e"
  [2]=>
  string(1) "e"
  [3]=>
  string(1) "k"
  [4]=>
  string(1) "s"
  [5]=>
  string(1) "f"
  [6]=>
  string(1) "o"
  [7]=>
  string(1) "r"
}

```

**程序二:**

```php
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array("Geeks", "for", "Geeks")
);

// Append the element into array
$arrItr->append("Computer");
$arrItr->append("Science");
$arrItr->append("Portal");

// Create copy of array iterator
$copyArr = $arrItr->getArrayCopy();

// Display the array element 
var_dump($copyArr);

?>
```

**输出:**

```php
array(6) {
  [0]=>
  string(5) "Geeks"
  [1]=>
  string(3) "for"
  [2]=>
  string(5) "Geeks"
  [3]=>
  string(8) "Computer"
  [4]=>
  string(7) "Science"
  [5]=>
  string(6) "Portal"
}

```

**参考:**[https://www . PHP . net/manual/en/arrayiterator . getarraycopy . PHP](https://www.php.net/manual/en/arrayiterator.getarraycopy.php)