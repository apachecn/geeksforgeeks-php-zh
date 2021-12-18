# PHP | array_udiff_assoc()函数

> 原文:[https://www . geesforgeks . org/PHP-array _ udiff _ assoc-function/](https://www.geeksforgeeks.org/php-array_udiff_assoc-function/)

array_udiff_assoc()是 PHP 中的一个内置函数，用于区分两个或多个数组。该函数通过使用带有附加键的用户定义函数来计算两个或多个数组的差数组，并返回差。它返回出现在第一个数组中而不出现在任何其他数组中的所有条目。它不同于 [array_diff_assoc()函数](https://www.geeksforgeeks.org/php-array_diff_assoc-function/)，因为它允许用户定义的函数决定标准。

**语法:**

> array_udiff_assoc($array1，$array2，$array3……数组 n，arr_udiffassocFun)

**使用的参数:**这个 array_udiff_assoc()函数参数描述如下:

1.  **数组 1 :** 它是初始数组，并与另一个数组进行比较。这是强制性的。
2.  **数组 2 :** 与第一个数组键比较的数组。这是强制性的。
3.  **数组 3 :** 第二个数组与第一个数组键比较。它是可选的。
4.  **arr _ udifassocfun:**定义自定义回调函数需要自定义函数和字符串，如果第一个参数比第二个参数大<、=、或>，则返回大于 0 的整数<、=、或>。

**返回值**:返回一个数组，该数组包含第一个数组的元素，这些元素在所有其他数组中都不存在。如果存在所有数组元素，则数组返回空值。
**注意:**这个内置函数 array_udiff_assoc())比较一个数组的键和用户自定义函数比较的值。该函数只检查 n 维数组的一维。

**例 1 :**

```
Input :
 $arr1 = array(
    "a" => "Geeks",
    "b" => "for",
    "d" => "geeks"
);
$arr2 = array(
    "a" => "Geeks",
    "y" => "is",
    "d" => "geeks"
);
Output:
Array
(
    [b] => for
)
Explanation: arr1 contains only one 
values(for) which is not present in 
arr2.

```

**例 2 :**

```
Input:
$arr1 = array(
    "a" => "C",
    "b" => "C++",
    "d" => "Java",
    "x" => "XML",
    "y" => "C#"
);
$arr2 = array(
    "a" => "C",
    "b" => "C++",
    "d" => "PHP",
    "x" => "Advanced PHP",
    "n" => "XML"    
);
Output:
Array
(
    [d] => Java
    [x] => XML
    [y] => C#
)

Explanation: arr1  return three values
(article) which are not present in arr2.
But XML is present both arr1 and arr2 
but both have different key.

```

让我们举一个简单的例子来理解 array_udiff_assoc()函数。

**程序 1:** 取两个数组(array1 和 array2)并使用用户自定义的键比较函数(arr _ udiffassocFun)。

```
<?php
<?php
// PHP code for array_udiff_assoc function.

// This function is used to decide which elements
// to pick array_udiff_assoc
function arr_udiffassocFun($x, $y)
{       
    return ($x === $y)? 0 : 1;
}

// array list for comparison.
$arr1 = array(
    "a" => "Raj",
    "b" => "Ram",
    "d" => "Denish",
    "r" => "David"
);
$arr2 = array(
    "a" => "Raj",
    "y" => "Ram",
    "d" => "Denish",
    "x" => "Ritche"
);

// Driver code
$result = array_udiff_assoc($arr1,
             $arr2, "arr_udiffassocFun");
print_r($result);
?>
```

**输出:**

```
Array
(
    [b] => Ram
    [r] => David
)

```

注:[b] = >因为密钥不同，所以打印 Ram。在 [array_diff_assoc()](https://www.geeksforgeeks.org/php-array_diff_assoc-function/) 和 array_udiff_assoc()中，键和值都进行了比较。 [array_diff()](https://www.geeksforgeeks.org/php-array_diff-function/) 仅比较值。

**程序:2** 取四个数组(array1、array2、array3 和 array4)并使用用户自定义的键比较函数 array_udiff_assoc()。

```
<?php
// PHP code for array_udiff_assoc function
// This function is used to decide which elements
// to pick array_udiff_assoc
function arr_udiffassocFun($x, $y)
{       
    return ($x === $y)? 0 : 1;
}

// array list for comparison.
$arr1 = array(
    "a" => "Larry",
    "b" => "Page",
    "d" => "Denish",
    "r" => "Ritche"
);
$arr2 = array(
    "a" => "Larry",
    "y" => "Page",
    "d" => "Denish",
    "r" => "Ritche"
);
$arr3 = array(
    "a" => "larry",
    "y" => "Bill Gate",
    "d" => "Denish",
    "r" => "Willion"
);
$arr4 = array(
    "a" => "Raj",
    "y" => "Bill Gate",
    "d" => "Denish",
    "r" => "Woks"
);
$result = array_udiff_assoc($arr1,
   $arr2, $arr3, $arr4, "arr_udiffassocFun");
// print result.
print_r($result);
?>
```

**输出:**

```
Array
(
    [b] => Page
)

```

**相关文章:**

*   [**PHP | arr_diff()函数:**](https://www.geeksforgeeks.org/php-array_diff-function/) 计算一个数组的差。
*   [**PHP | arr_udiff()函数:**](https://www.geeksforgeeks.org/php-array_udiff-function/) 通过使用用户定义的回调函数计算数组的差异并比较数据。
*   [**PHP | array_diff_assoc()函数:**](https://www.geeksforgeeks.org/php-array_diff_assoc-function/) 用额外的索引键计算数组的差异。
*   [**PHP | array _ diff _ uasoc()函数:**](https://www.geeksforgeeks.org/php-array_diff_uassoc-function/) 该函数比较一个或多个数组之间的键和值，并返回第一个数组中不在其余数组中的元素。
*   [**PHP | array_diff_key()函数:**](https://www.geeksforgeeks.org/php-array_diff_key-function/) 将第一个参数数组的键与其余数组进行比较，并返回一个数组，该数组包含$array1 中不存在于任何其他数组中的所有条目。

**练习类似问题 On:** [**PHP**](https://practice.geeksforgeeks.org/topics/PHP)
参考文献:[http://php.net/manual/en/function.array-udiff-assoc.php](http://php.net/manual/en/function.array-udiff-assoc.php)