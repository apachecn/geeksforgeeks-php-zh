# PHP | ArrayIterator uksort()函数

> 原文:[https://www . geeksforgeeks . org/PHP-arrayiterator-uksort-function/](https://www.geeksforgeeks.org/php-arrayiterator-uksort-function/)

**ArrayIterator::uksort()函数**是 PHP 中的一个内置函数，用于通过使用用户定义的比较函数对键进行排序。

**语法:**

```php
*void* ArrayIterator::uksort( *callable* $cmp_function )
```

**参数:**该功能接受单参数 **$cmp_function** ，保存用户定义的比较函数。

**返回值:**该函数不返回值。

下面的程序说明了 PHP 中的 ArrayIterator::uksort()函数:
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

// User defined comparator function 
function sorting($a, $b) { 
    if($a == $b)
        return 0; 
    return ($a < $b) ? -1 : 1; 
} 

$arrItr->uksort("sorting"); 

// Printing the sorted array. 
print_r($arrItr); 

?>
```

**Output:**

```php
ArrayIterator Object
(
    [storage:ArrayIterator:private] => Array
        (
            [a] => 4
            [b] => 2
            [d] => 6
            [e] => 1
            [f] => 9
            [g] => 8
        )

)

```

**程序 2:**

```php
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array(
        "b" => "for",
        "a" => "Geeks",
        "e" => "Science",
        "c" => "Geeks",
        "f" => "Portal",
        "d" => "Computer"
    )
);

// Declare a comparison function to sort  
// values in descending order 
function comparison($val1, $val2) { 
    if ($val1 == $val2) { 
        return 0; 
    } 
    else if($val1 > $val2) 
        return -1; 
    else
        return 1; 
} 

$arrItr->uksort('comparison'); 

// Print the sorted ArrayObject 
print_r($arrItr); 

?>
```

**Output:**

```php
ArrayIterator Object
(
    [storage:ArrayIterator:private] => Array
        (
            [f] => Portal
            [e] => Science
            [d] => Computer
             => Geeks
            [b] => for
            [a] => Geeks
        )

)

```

**参考:**T2】https://www.php.net/manual/en/arrayiterator.uksort.php