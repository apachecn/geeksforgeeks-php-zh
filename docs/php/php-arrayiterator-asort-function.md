# PHP | ArrayIterator asort()函数

> 原文:[https://www . geeksforgeeks . org/PHP-arrayiterator-asort-function/](https://www.geeksforgeeks.org/php-arrayiterator-asort-function/)

**数组运算符::asort()函数**是 PHP 中的一个内置函数，用于对数组值进行排序。

**语法:**

```
*void* ArrayIterator::asort( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数不返回值。

下面的程序说明了 PHP 中的 ArrayIterator::asort()函数:

**程序 1:**

```
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array('G', 'e', 'e', 'k', 's', 'f', 'o', 'r')
);

// Append the element into array iterator
$arrItr->asort();

// Display the elements
while($arrItr->valid()) {
    echo $arrItr->current();
    $arrItr->next();
}

?>
```

**输出:**

```
Geefkors

```

**程序二:**

```
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array("Geeks", "for", "Geeks")
);

// Append the array element
$arrItr->asort();

// Disaply the elements
foreach ($arrItr as $key => $val) {
    echo $key . " => " . $val . "\n";
}

?>
```

**输出:**

```
0 => Geeks
2 => Geeks
1 => for

```

**参考:**T2】https://www.php.net/manual/en/arrayiterator.asort.php