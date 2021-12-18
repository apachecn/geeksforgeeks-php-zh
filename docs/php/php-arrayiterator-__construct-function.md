# PHP | ArrayIterator _ _ construct()函数

> 原文:[https://www . geeksforgeeks . org/PHP-arrayiterator-_ _ construct-function/](https://www.geeksforgeeks.org/php-arrayiterator-__construct-function/)

**数组运算符::__construct()函数**是 PHP 中的一个内置函数，用于构造一个数组运算符。

**语法:**

```
*public* ArrayIterator::__construct( *mixed* $array, *int* $flags = 0 )
```

**参数:**这个函数接受两个参数，如上所述，如下所述:

*   **$ array:** This parameter holds the array or array of object iterators.
*   **$ flag:** This parameter controls the behavior of array generator objects.

**返回值:**该函数返回 ArrayIterator 对象。

下面的程序说明了 PHP 中的 ArrayIterator::__construct()函数:

**程序 1:**

```
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array('G', 'e', 'e', 'k', 's', 'f', 'o', 'r'),
    ArrayIterator::ARRAY_AS_PROPS
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
    array("Geeks", "for", "Geeks"), 
    ArrayIterator::STD_PROP_LIST
);

// Display the elements
foreach ($arrItr as $key => $val) {
    echo $key . " => " . $val . "\n";
}

?>
```

**输出:**

```
0 => Geeks
1 => for
2 => Geeks

```

**参考:**T2】https://www.php.net/manual/en/arrayiterator.construct.php