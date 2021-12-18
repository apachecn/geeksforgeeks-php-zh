# PHP | array_multisort()函数

> 原文:[https://www.geeksforgeeks.org/php-array_multisort-function/](https://www.geeksforgeeks.org/php-array_multisort-function/)

array _ multi sort()是 PHP 中的一个内置函数，用于一次对多个数组进行排序，或者对每个维度都有一个多维数组进行排序。
有了这个功能，要记住会保留字符串键，但是数字键会重新索引，从 0 开始增加 1。

**语法:**

```
*bool* array_multisort($array1, sorting_order, sorting_type, $array2..)
```

**参数:**数组一般取一个参数，就是需要排序的数组。但是除此之外，这个函数还可以带两个可选参数 sorting_order 和 sorting_type。

1.  **$array1** :此参数指定我们要排序的数组。
2.  **排序 _ 顺序**:此参数指定使用的顺序，即升序或降序。该参数的默认值为 SORT_ASC。也就是按升序排序。为了按降序排序，我们必须将此参数设置为 SORT_DESC。
3.  **sorting_type**: This parameter specifies the sort options for the arrays and they are as follows:
    *   SORT_REGULAR:定期比较元素(标准 ASCII)。
    *   将元素作为数值进行比较。
    *   将元素作为字符串值进行比较。
    *   基于当前区域设置，将元素作为字符串进行比较。
    *   SORT_NATURAL:使用“自然排序”将元素作为字符串进行比较。
    *   SORT_FLAG_CASE:可以与 SORT_STRING 或 SORT_NATURAL 组合(按位“或”)，对字符串进行不区分大小写的排序。

    如果我们想对多个数组进行排序，我们可以将它们作为参数传递，如$array2、$array3…后跟它们的 sorting_order、sorting_type。

**返回值:**array _ multisort()函数返回一个布尔值。也就是说，它将在成功时返回**真**，在失败时返回**假**。

**注意:**如果比较时两个成员相等，那么它们在排序数组中的相对顺序是未定义的。

下面的程序说明了 array_multisort()函数:

**程序 1:**

```
<?php

// Input array
$animals = array("Dog", "Cat", "Horse", 
                "Bear", "Zebra", "Lion");

// sorting array using default values
// for sorting_order and sorting_type    
array_multisort($animals);

print_r($animals);

?>
```

输出:

```
Array
(
    [0] => Bear
    [1] => Cat
    [2] => Dog
    [3] => Horse
    [4] => Lion
    [5] => Zebra
)

```

**程序 2:**

```
<?php

// Input arrays
$array1=array("Dog", "Cat");
$array2=array("Fido", "Missy");

// sorting multiple arrays using default values
// for sorting_order and sorting_type         
array_multisort($array1, $array2);

// printing sorted arrays         
print_r($array1);
print_r($array2);

?> 
```

输出:

```
Array
(
    [0] => Cat
    [1] => Dog
)
Array
(
    [0] => Missy
    [1] => Fido
)

```

**程序 3:**

```
<?php

// Input arrays
$array1=array("Dog", "Dog", "Cat");
$array2=array("Pluto", "Fido", "Missy");

// sorting multiple arrays       
array_multisort($array1, SORT_ASC, $array2, SORT_DESC);

// Printing sorted arrays       
print_r($array1);
print_r($array2);

?> 
```

输出:

```
Array
(
    [0] => Cat
    [1] => Dog
    [2] => Dog
)
Array
(
    [0] => Missy
    [1] => Pluto
    [2] => Fido
)

```

**参考**:
T3】http://php.net/manual/en/function.array-multisort.php