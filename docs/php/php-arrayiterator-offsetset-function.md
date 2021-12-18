# PHP | ArrayIterator offset()函数

> 原文:[https://www . geesforgeks . org/PHP-arrayiterator-offset set-function/](https://www.geeksforgeeks.org/php-arrayiterator-offsetset-function/)

**ArrayIterator::offset()函数**是 PHP 中的一个内置函数，用于设置偏移量的值。

**语法:**

```php
*void* ArrayIterator::offsetSet( *mixed* $index, *mixed* $newval )
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **$ index:** This parameter stores the index of the set offset.
*   **$ newval:** This parameter holds the new value to be stored at the given index.

**返回值:**该函数不返回值。

下面的程序说明了 PHP 中的 ArrayIterator::offset()函数:

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

// Update the value at index 1 
$arrItr->offsetSet("g", "Geeks"); 

// Print the updated ArrayObject 
print_r($arrItr); 

?>
```

**输出:**

```php
ArrayIterator Object
(
    [storage:ArrayIterator:private] => Array
        (
            [a] => 4
            [b] => 2
            [g] => Geeks
            [d] => 6
            [e] => 1
            [f] => 9
        )

)

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

// Update the value at index 1 
$arrItr->offsetSet(1, "GeeksforGeeks"); 

// Print the updated ArrayObject 
print_r($arrItr); 

?>
```

**输出:**

```php
ArrayIterator Object
(
    [storage:ArrayIterator:private] => Array
        (
            [0] => for
            [1] => GeeksforGeeks
            [2] => Science
            [3] => Geeks
            [4] => Portal
            [5] => Computer
        )

)

```

**参考:**T2】https://www.php.net/manual/en/arrayiterator.offsetset.php