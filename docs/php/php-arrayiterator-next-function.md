# PHP | ArrayIterator next()函数

> 原文:[https://www . geeksforgeeks . org/PHP-arrayiterator-next-function/](https://www.geeksforgeeks.org/php-arrayiterator-next-function/)

**ArrayIterator::next()函数**是 PHP 中的一个内置函数，用于将迭代器移动到下一个条目。

**语法:**

```
*void* ArrayIterator::next( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数不返回值。

下面的程序说明了 PHP 中的 ArrayIterator::next()函数:

**程序 1:**

```
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array('G', 'e', 'e', 'k', 's', 'f', 'o', 'r')
);

// Display the elements
while($arrItr->valid()) {
    echo $arrItr->current();
    $arrItr->next();
}

?>
```

**输出:**

```
Geeksfor

```

**程序二:**

```
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array("Geeks", "for", "Geeks")
);

// Display value of array iterator
echo $arrItr->current() . "\n";

// Use next() function to move
// element into next position
$arrItr->next();

// Display value of array iterator
echo $arrItr->current() . "\n";

// Use next() function to move
// element into next position
$arrItr->next();

// Display value of array iterator
echo $arrItr->current();

?>
```

**输出:**

```
Geeks
for
Geeks

```

**参考:**T2】https://www.php.net/manual/en/arrayiterator.next.php