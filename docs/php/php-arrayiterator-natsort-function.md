# PHP | ArrayIterator natsort()函数

> 原文:[https://www . geeksforgeeks . org/PHP-arrayiterator-natsort-function/](https://www.geeksforgeeks.org/php-arrayiterator-natsort-function/)

**ArrayIterator::natsort()函数**是 PHP 中的一个内置函数，用来对数组进行自然排序。

**语法:**

```php
*void* ArrayIterator::natsort( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数不返回值。

下面的程序说明了 PHP 中的 ArrayIterator::natsort()函数:

**程序 1:**

```php
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array(
        5 => 'G',
        4 => 'e',
        3 => 'E',
        2 => 'k',
        1 => 'S', 
    )
);

// Sort the array key
$arrItr->natsort();

// Display the element
while($arrItr->valid()) {
    echo $arrItr->current() . " ";
    $arrItr->next();
}

?>
```

**输出:**

```php
E G S e k

```

**程序二:**

```php
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array("geeks", "GEEKS", "Geeks", "gEEKS")
);

// Sort the array with case sensitive
$arrItr->natsort();

var_dump($arrItr);

?>
```

**输出:**

```php
object(ArrayIterator)#1 (1) {
  ["storage":"ArrayIterator":private]=>
  array(4) {
    [1]=>
    string(5) "GEEKS"
    [2]=>
    string(5) "Geeks"
    [3]=>
    string(5) "gEEKS"
    [0]=>
    string(5) "geeks"
  }
}

```

**参考:**T2】https://www.php.net/manual/en/arrayiterator.natsort.php