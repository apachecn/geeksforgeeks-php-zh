# PHP | array_intersect_key()函数

> 原文:[https://www . geesforgeks . org/PHP-array _ intersect _ key-function/](https://www.geeksforgeeks.org/php-array_intersect_key-function/)

PHP 的这个内置函数用于计算两个或多个数组的交集。该函数与 [array_intersect()](https://www.geeksforgeeks.org/php-array_intersect-function/) 和 [array_intersect_assoc()](https://www.geeksforgeeks.org/php-array_intersect_assoc-function/) 的不同之处在于，它使用键进行比较，并返回匹配的键元素。该函数只打印第一个数组中那些键与所有其他数组中的元素相匹配的元素。
可以参考 [array_intersect()](https://www.geeksforgeeks.org/php-array_intersect-function/) 和 [array_intersect_assoc()](https://www.geeksforgeeks.org/php-array_intersect_assoc-function/) 来更好的理解。

**语法:**

```php
*array* array_intersect_key($array1, $array2, $array3, $array4...)

```

**参数:**array _ intersect _ key()函数至少取两个数组作为参数。它可以采用任意数量的大于或等于两个的数组，用逗号(“，”)分隔。

**返回类型:**函数返回另一个数组，该数组包含第一个数组的元素，这些元素存在于作为参数传递的所有其他数组中，这些数组的键相互匹配。如果没有匹配的关键字，则返回空数组。

示例:

```php
Input : $array1 = ("1" => "aakash", "2" => "rishav", "3" => "gaurav")
        $array2 = ("1" => "shyam", "2" => "rishi", "5" => "rishav")
        $array3 = ("1" => "aakash", "4" => "raghav", "2" => "ravi")
Output :
        Array
        (
          [1] => aakash
          [2] => rishav
        )

```

下面的程序说明了 array_intersect_key()函数。在下面的程序中，我们已经使用了 array_intersect_key()来查找数组之间的交集。让我们仔细看看 [array_intersect()](https://www.geeksforgeeks.org/php-array_intersect-function/) 和 [array_intersect_assoc()](https://www.geeksforgeeks.org/php-array_intersect_assoc-function/) 的这个和其他函数的输出，以了解它们的区别。

```php
<?php

// PHP program to illustrate the use 
// of array_intersect_key() function

$array1 = array("1" => "aakash", "2" => "rishav", "3" => "gaurav");
$array2 = array("1" => "shyam", "2" => "rishi", "5" => "rishav");
$array3 = array("1" => "aakash", "4" => "raghav", "2" => "ravi");

print_r(array_intersect_key($array1, $array2, $array3));

?>
```

输出:

```php
Array
(
    [1] => aakash
    [2] => rishav
)
```

**参考**:
T3】http://php.net/manual/en/function.array-intersect-key.php