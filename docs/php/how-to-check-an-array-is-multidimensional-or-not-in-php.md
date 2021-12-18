# 在 PHP 中如何检查一个数组是不是多维的？

> 原文:[https://www . geesforgeks . org/如何检查数组是多维的还是非多维的 php/](https://www.geeksforgeeks.org/how-to-check-an-array-is-multidimensional-or-not-in-php/)

给定一个数组(一维或多维)，任务是检查给定的数组是否是多维的。很少有方法可以检查数组是否是多维的。函数 **[count()](https://www.geeksforgeeks.org/php-count-function/)** 和 **count_recursive()** 如果数组包含一个空的子数组，而另一个子数组使用的是 [rsort()](https://www.geeksforgeeks.org/php-rsort-function/) 函数，则会给出错误的结果。该函数将所有子数组向父数组的开头排序，并对数组进行重新索引。这确保了如果父数组中有一个或多个子数组，父数组的第一个元素(在索引 0 处)将始终是一个数组。检查索引 0 处的元素，我们可以知道数组是否是多维的。

**语法:**

```php
rsort( $array )
```

**参数:**[rsort()](https://www.geeksforgeeks.org/php-rsort-function/)函数接受一个参数。

*   **$ array:** This is the object you want to pass to the function.

**示例 1:** 使用 **rsort** 函数检查数组是否为多维数组的 PHP 程序。

```php
<?php
$myarray = array( 

    // Default key for each will 
    // start from 0 
    array("Geeks", "For", "Geeks"), 
    array("Hello", "World") 
); 

// Function to check array is
// multi-dimensional or not
function is_multi_array( $arr ) {
    rsort( $arr );
    return isset( $arr[0] ) && is_array( $arr[0] );
}

// Display result
var_dump( is_multi_array( $myarray ) );
?>
```

**输出:**

```php
bool(true)

```