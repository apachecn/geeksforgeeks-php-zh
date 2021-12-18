# PHP | ArrayIterator getFlags()函数

> 原文:[https://www . geeksforgeeks . org/PHP-arrayiterator-getflags-function/](https://www.geeksforgeeks.org/php-arrayiterator-getflags-function/)

**ArrayIterator::getFlags()函数**是 PHP 中的一个内置函数，用来获取数组迭代器的标志行为。

**语法:**

```
*int* ArrayIterator::getFlags( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数返回数组运算符的行为标志。

下面的程序说明了 PHP 中的 ArrayIterator::getFlags()函数:

**程序 1:**

```
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array('G', 'e', 'e', 'k', 's', 'f', 'o', 'r')
);

// Get the flag
$flag = $arrItr->getFlags();

// Display the flag
var_dump($flag);

?>
```

**输出:**

```
int(0)

```

**程序二:**

```
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array("Geeks", "for", "Geeks")
);

// Append the element into array
$arrItr->append("Computer");
$arrItr->append("Science");
$arrItr->append("Portal");

// Get the flag
$flag = $arrItr->getFlags();

// Display the flag value
var_dump($flag);

?>
```

**输出:**

```
int(0)

```

**参考:**T2】https://www.php.net/manual/en/arrayiterator.getflags.php