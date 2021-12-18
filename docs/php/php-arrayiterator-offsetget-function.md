# PHP | ArrayIterator offsetGet()函数

> 原文:[https://www . geeksforgeeks . org/PHP-arrayiterator-offset get-function/](https://www.geeksforgeeks.org/php-arrayiterator-offsetget-function/)

**ArrayIterator::offsetGet()函数**是 PHP 中的一个内置函数，用于获取偏移量的值。

**语法:**

```
*mixed* ArrayIterator::offsetGet( *mixed* $index )
```

**参数:**该函数接受单个参数 **$index** ，该参数保存从中获取值的偏移量。

**返回值:**该函数返回偏移索引处的值。

下面的程序说明了 PHP 中的 ArrayIterator::offsetGet()函数:

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

// Value present at index "a" 
echo ($arrItr->offsetGet("a")) . " "; 

// Value present at index "g"
echo ($arrItr->offsetGet("g")) . " "; 

// Value present at index "f"
echo ($arrItr->offsetGet("f")); 

?>
```

**输出:**

```
4 8 9

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

// Print the value at index 0
echo $arrItr->offsetGet(0) . "\n"; 

// Print the value at index 3
echo $arrItr->offsetGet(3); 

?>
```

**输出:**

```
Geeks
for
Geeks

```

**参考:**T2】https://www.php.net/manual/en/arrayiterator.offsetget.php