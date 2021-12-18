# PHP | array_intersect_assoc()函数

> 原文:[https://www . geesforgeks . org/PHP-array _ intersect _ assoc-function/](https://www.geeksforgeeks.org/php-array_intersect_assoc-function/)

array_intersect_assoc()是 PHP 中的一个内置函数，用于计算两个或多个数组的交集。这个函数类似于文章 [PHP | array_intersect()函数](https://www.geeksforgeeks.org/php-array_intersect-function/)中讨论的函数 array_intersect()。该函数还用于比较两个或多个数组的值，并返回匹配项。唯一的区别是，该函数返回第一个数组的所有值，这些值出现在与第一个数组索引相同的所有其他参数中，即键主要用于比较。

**语法:**

```
*array* array_intersect_assoc($array1, $array2, $array3,...)

```

**参数:**array _ intersect _ assoc()函数将至少两个数组作为参数。该函数可以将任意数量的数组作为大于或等于 2 的参数。

**返回值:**函数返回另一个包含所有输入数组交集的数组。如果没有元素匹配，则返回空数组。

示例:

```
Input : 
       $array1 = ("1" => "shyam", "2" => "rishav", "3" => "gaurav");
       $array2 = ("1" => "shyam", "2" => "rishi", "3" => "rishav");
       $array3 = ("1" => "shyam", "2" => "rishav", "3" => "ravi");
Output :
       Array
       (
           [1] => shyam
       )

```

在下面的程序中，我们使用了 array_intersect_assoc()来寻找数组之间的交集。让我们仔细看看这个和 array_intersect()函数的输出。

```
<?php

// PHP function to illustrate the use of array_intersect_assoc()
function Intersect($array1, $array2, $array3)
{
    $result = array_intersect_assoc($array1, $array2, $array3);
    return($result);
}

$array1 = array("1" => "shyam", "2" => "rishav", "3" => "gaurav");
$array2 = array("1" => "shyam", "2" => "rishi", "3" => "rishav");
$array3 = array("1" => "shyam", "2" => "rishav", "3" => "ravi");
print_r(Intersect($array1, $array2, $array3));

?>
```

输出:

```
Array
(
    [1] => shyam
)

```

在上面的程序中，我们使用了 array_intersect_assoc()来寻找数组的交集。在下面的程序中，我们将使用 array_intersect()函数来做同样的事情。密切关注两个程序的输出。与 array_intersect()不同，第一个函数只返回严格相似的元素，包括值和键。

```
<?php

// PHP function to illustrate the use of array_intersect()
function Intersect($array1, $array2, $array3)
{
    $result = array_intersect($array1, $array2, $array3);
    return($result);
}

$array1 = array("1" => "shyam", "2" => "rishav", "3" => "gaurav");
$array2 = array("1" => "shyam", "2" => "rishi", "3" => "rishav");
$array3 = array("1" => "shyam", "2" => "rishav", "3" => "ravi");
print_r(Intersect($array1, $array2, $array3));

?>
```

输出:

```
Array
(
    [1] => shyam
    [2] => rishav
)

```

**参考**:[http://php.net/manual/en/function.array-intersect-assoc.php](http://php.net/manual/en/function.array-intersect-assoc.php)