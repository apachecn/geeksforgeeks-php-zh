# PHP | array_intersect()函数

> 原文:[https://www.geeksforgeeks.org/php-array_intersect-function/](https://www.geeksforgeeks.org/php-array_intersect-function/)

PHP 的这个内置函数用于计算两个或多个数组的交集。该函数用于比较两个或多个数组的值，并返回匹配项。该函数只打印第一个数组中出现在所有其他数组中的元素。

**语法:**

```php
*array* array_intersect($array1, $array2, $array3, $array4...)
```

**参数**:array _ intersect()函数至少取两个数组作为自变量。它可以采用任意数量的大于或等于两个的数组，用逗号(“，”)分隔。

**返回类型**:该函数返回另一个数组，该数组包含第一个数组的元素，这些元素存在于作为参数传递的所有其他数组中。如果没有元素匹配，则返回空数组。

**注**:保留元素的键。也就是说，输出数组中元素的键将与第一个数组中那些元素的键相同。

示例:

```php
Input : $array1 = array(5, 10, 15, 20, 25, 30)
        $array2 = array(20, 10, 15, 55, 110, 30)
        $array3 = array(10, 15, 30, 55, 100, 95)
Output :
        Array
        (
           [1] => 10
           [2] => 15
           [5] => 30
        )

Input : $array1 = array("ram", "laxman", "rishi", "ayush");
        $array2 = array("ayush", "gaurav", "rishi", "rohan");
        $array3 = array("rishi", "gaurav", "ayush", "ravi");
Output :
        Array
        (
           [2] => rishi
           [3] => ayush
        )

```

下面的程序说明了 PHP 中的 array_intersect()函数:

```php
<?php

// PHP function to illustrate the use of array_intersect()
function Intersect($array1, $array2, $array3)
{
    $result = array_intersect($array1, $array2, $array3);
    return($result);
}

$array1 = array(5, 10, 15, 20, 25, 30);
$array2 = array(20, 10, 15, 55, 100, 110, 30);
$array3 = array(10, 15, 30, 55, 100, 95);
print_r(Intersect($array1, $array2, $array3));

?>

```

输出:

```php
Array
(
    [1] => 10
    [2] => 15
    [5] => 30
)

```

**参考**:[http://php.net/manual/en/function.array-intersect.php](http://php.net/manual/en/function.array-intersect.php)