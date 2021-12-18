# PHP | ArrayIterator offset exists()函数

> 原文:[https://www . geeksforgeeks . org/PHP-arrayiterator-offset exists-function/](https://www.geeksforgeeks.org/php-arrayiterator-offsetexists-function/)

**ArrayIterator::offsetExists()函数**是 PHP 中的一个内置函数，用于检查给定索引处是否存在偏移量。

**语法:**

```
*bool* ArrayIterator::offsetExists( *mixed* $index )
```

**参数:**该功能接受单个参数 **$index** ，保存索引值，检查偏移的存在。

**返回值:**如果存在偏移，该函数返回真，否则返回假。

下面的程序说明了 PHP 中的 ArrayIterator::offsetExists()函数:

**程序 1:**

```
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array(
        "a" => 4,
        "b" => 2,
        "g" => 8,
        "d" => 6,
        "e" => 1,
        "f" => 9
    )
);

// Display the offset value
var_dump($arrItr->offsetGet("a")); 

// Check the existence of offset
var_dump($arrItr->offsetExists("a"));

// Unset the offset value
var_dump($arrItr->offsetUnset("a"));

// Check the existence of offset
var_dump($arrItr->offsetExists("a"));

?>
```

**输出:**

```
int(4)
bool(true)
NULL
bool(false)

```

**程序二:**

```
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array(
        "for", "Geeks", "Science",
        "Geeks", "Portal", "Computer"
    )
);

// Print the value at index 1 
echo $arrItr->offsetGet(1) . "\n"; 

// Check the existence of offset
var_dump($arrItr->offsetExists(1));

// Unset the offset value
var_dump($arrItr->offsetUnset(1));

// Check the existence of offset
var_dump($arrItr->offsetExists(1));

// Print the value at index 0
echo $arrItr->offsetGet(0) . "\n";

// Check the existence of offset
var_dump($arrItr->offsetExists(0));

// Unset the offset value
var_dump($arrItr->offsetUnset(0));

// Check the existence of offset
var_dump($arrItr->offsetExists(0));

?>
```

**输出:**

```
Geeks
bool(true)
NULL
bool(false)
for
bool(true)
NULL
bool(false)

```

**参考:**[https://www . PHP . net/manual/en/arrayiterator . offset exists . PHP](https://www.php.net/manual/en/arrayiterator.offsetexists.php)