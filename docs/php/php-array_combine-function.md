# PHP | array_combine()函数

> 原文:[https://www.geeksforgeeks.org/php-array_combine-function/](https://www.geeksforgeeks.org/php-array_combine-function/)

array_combine()是 PHP 中的一个内置函数，用于组合两个数组，并通过使用一个数组作为键，另一个数组作为值来创建一个新数组。也就是说，一个数组的所有元素将是新数组的键，第二个数组的所有元素将是这个新数组的值。

**例:**

```
Input : $array1 = ("Ram", "Akash", "Rishav"); 
        $array2 = ('24', '30', '45');
Output :
        Array
        (
          [Ram] => 24
          [Akash] => 30
          [Rishav] => 45
        )

Input : $array1 = ("65824", "92547", "12045");
        $array2 = ('1', '2', '3');
Output :
        Array
        (
          [65824] => 1
          [92547] => 2
          [12045] => 3
        )

```

**语法:**

```
array_combine( $keys_array, $values_array )
```

**参数:**该功能接受两个参数，两个都是强制的。功能参数如下:

*   **$ keys _ array:** This is an array of keys. If the illegal value is passed as a key, it will be converted into a string.
*   **$ values _ array:** This is the array of values to be used in the new array.

**返回值:**该函数返回一个新的组合数组，其中第一个数组 *$keys_array* 中的元素代表新数组中的键，第二个数组 *$values_array* 中的元素代表新数组中相应的值。如果两个数组中的元素数量不同，此函数将返回 false。

下面的程序说明了 PHP 中的 array_combine()函数:

```
<?php

// PHP program to illustrate the working
// of array_combine() function
function Combine($array1, $array2) {
    return(array_combine($array1, $array2));
}

// Driver Code
$array1 = array("Ram", "Akash", "Rishav");
$array2 = array('24', '30', '45');

print_r(Combine($array1, $array2));
?>
```

**输出:**

```
Array
(
    [Ram] => 24
    [Akash] => 30
    [Rishav] => 45
)

```

**注意:**两个数组中的元素总数必须相等，函数才能成功执行，否则会抛出错误。

**参考:**T2】https://www.php.net/manual/en/function.array-combine.php