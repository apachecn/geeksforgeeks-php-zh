# PHP | ArrayIterator count()函数

> 原文:[https://www . geeksforgeeks . org/PHP-arrayiterator-count-function/](https://www.geeksforgeeks.org/php-arrayiterator-count-function/)

**ArrayIterator::count()函数**是 PHP 中的一个内置函数，用于对数组迭代器的元素进行计数。

**语法:**

```php
*int* ArrayIterator::count( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**这个函数返回数组迭代器中存在的元素个数。

下面的程序说明了 PHP 中的 ArrayIterator::count()函数:

**程序 1:**

```php
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array('G', 'e', 'e', 'k', 's')
);

// Count the element into array iterator
echo $arrItr->count();

?>
```

**输出:**

```php
5

```

**程序二:**

```php
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array("Geeks", "for", "Geeks"), 
    ArrayIterator::STD_PROP_LIST
);

// Count the array element
echo $arrItr->count();

?>
```

**输出:**

```php
3

```

**参考:**T2】https://www.php.net/manual/en/arrayiterator.count.php