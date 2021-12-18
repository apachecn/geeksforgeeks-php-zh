# PHP | array_diff()函数

> 原文:[https://www.geeksforgeeks.org/php-array_diff-function/](https://www.geeksforgeeks.org/php-array_diff-function/)

array_diff()是 PHP 中的一个内置函数，用于计算两个或多个数组之间的差异。该函数根据元素的值计算一个或多个数组之间的差，并以新数组的形式返回差。这个函数基本上返回第一个数组中所有其他数组中没有的条目。

**语法:**

```php
array_diff($array1, $array2, $array3, ...,$arrayn)

```

**参数**:函数可以取任意数量的数组作为需要比较的参数。

**返回类型**:该函数将参数中的第一个数组与其余数组进行比较，并返回一个包含$array1 中所有条目的数组，这些条目在任何其他数组中都不存在。

示例:

```php
Input :  $array1 = ('a', 'b', 'c');
         $array2 = ('a', 'd', 'e');
         $array3 = ('a', 'b', 'f');
         array_diff($array1, $array2, $array3); 
Output :
         Array
         (
           [2] => c
         )

Input : $array1 = ('a', 'b', 'a');
        $array2 = ('a', 'd', 'e');
Output :
         Array
         (
           [1] => b
         )

```

下面的程序说明了 PHP 中 array_diff()的工作方式:

```php
<?php
// PHP code to illustrate the working of array_diff()
function Difference($array1, $array2, $array3){
    return(array_diff($array1, $array2, $array3));
}

// Driver Code
$array1 = array('a', 'b', 'c', 'd', 'e', 'f');
$array2 = array('a', 'b', 'g', 'h');
$array3 = array('a', 'f', 'i');
print_r(Difference($array1, $array2, $array3));
?>
```

输出:

```php
Array
(
    [2] => c
    [3] => d
    [4] => e
)

```

**需要注意的重要点** :

*   It compares the string representations of elements. That is, for array_diff (), 1 and "1" are both equal.
*   It doesn't matter how many times the first array element repeats. That is to say, if an element appears three times in $array1 and only once in other arrays, all three occurrences of the element in the first array will be omitted in the output.
*   For multidimensional arrays, we need to compare each dimension separately. Examples:-$array1[2], $array2[2], etc.

**参考**:[http://php.net/manual/en/function.array-diff.php](http://php.net/manual/en/function.array-diff.php)