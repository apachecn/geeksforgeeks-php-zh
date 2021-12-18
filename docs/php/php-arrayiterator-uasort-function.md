# PHP | ArrayIterator uasort()函数

> 原文:[https://www . geeksforgeeks . org/PHP-arrayiterator-uasort-function/](https://www.geeksforgeeks.org/php-arrayiterator-uasort-function/)

**ArrayIterator::uasort()函数**是 PHP 中的一个内置函数，用于使用用户定义的比较函数对元素进行排序，并维护它们的索引关联。

**语法:**

```
*void* ArrayIterator::uasort( *callable* $cmp_function )
```

**参数:**该函数接受单个参数 **$cmp_function** ，这是用户自定义的比较函数。此比较函数接受两个参数，即 ArrayIterator 的值，如果第一个参数小于、等于或大于零，则分别返回小于、等于或大于零的值。

**返回值:**该函数不返回值。

下面的程序说明了 PHP 中的 ArrayIterator::uasort()函数:
strong >程序 1:

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

// User defined comparator function 
function sorting($a, $b) { 
    if($a == $b)
        return 0; 
    return ($a < $b) ? -1 : 1; 
} 

$arrItr->uasort("sorting"); 

// Printing the sorted array. 
print_r($arrItr); 

?>
```

**Output:**

```
ArrayIterator Object
(
    [storage:ArrayIterator:private] => Array
        (
            [e] => 1
            [b] => 2
            [a] => 4
            [d] => 6
            [g] => 8
            [f] => 9
        )

)

```

**程序 2:**

```
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array(
        "a" => "Geeks",
        "b" => "for",
        "c" => "Geeks",
        "d" => "Computer",
        "e" => "Science",
        "f" => "Portal"
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

$arrItr->uasort('comparison'); 

// Print the sorted ArrayObject 
print_r($arrItr); 

?>
```

**Output:**

```
ArrayIterator Object
(
    [storage:ArrayIterator:private] => Array
        (
            [b] => for
            [e] => Science
            [f] => Portal
            [a] => Geeks
             => Geeks
            [d] => Computer
        )

)

```

**参考:**T2】https://www.php.net/manual/en/arrayiterator.uasort.php