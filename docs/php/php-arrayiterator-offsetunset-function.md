# PHP | ArrayIterator offset()函数

> 原文:[https://www . geeksforgeeks . org/PHP-arrayiterator-offsetunset-function/](https://www.geeksforgeeks.org/php-arrayiterator-offsetunset-function/)

**ArrayIterator::offsetUnset()函数**是 PHP 中的一个内置函数，用于取消设置偏移量的值。

**语法:**

```php
*void* ArrayIterator::offsetUnset( *mixed* $index )
```

**参数:**该函数接受单个参数 **$index** ，该参数保存索引以取消偏移设置。

**返回值:**该函数不返回值。

下面的程序说明了 PHP 中的 ArrayIterator::offsetUnset()函数:

**程序 1:**

```php
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

// Unset the offset value
var_dump($arrItr->offsetUnset("a"));

// Display the offset value
var_dump($arrItr->offsetGet("g")); 

// Unset the offset value
var_dump($arrItr->offsetUnset("g"));

// Display the offset value
var_dump($arrItr->offsetGet("f")); 

// Unset the offset value
var_dump($arrItr->offsetUnset("f"));

?>
```

**输出:**

```php
int(4)
NULL
int(8)
NULL
int(9)
NULL

```

**程序二:**

```php
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

// Unset the offset value
var_dump($arrItr->offsetUnset(1));

// Print the value at index 0
echo $arrItr->offsetGet(0) . "\n";

// Unset the offset value
var_dump($arrItr->offsetUnset(0));

// Print the value at index 3
echo $arrItr->offsetGet(3) . "\n"; 

// Unset the offset value
var_dump($arrItr->offsetUnset(3));

?>
```

**输出:**

```php
Geeks
NULL
for
NULL
Geeks
NULL

```

**参考:**T2】https://www.php.net/manual/en/arrayiterator.offsetunset.php