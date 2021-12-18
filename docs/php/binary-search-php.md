# PHP 中的二分搜索法

> 原文:[https://www.geeksforgeeks.org/binary-search-php/](https://www.geeksforgeeks.org/binary-search-php/)

[二分搜索法](https://www.geeksforgeeks.org/binary-search/)是一种搜索技术，用于搜索排序数组中的元素。在本文中，我们将学习如何使用迭代和递归的方式在 PHP 中实现二分搜索法。给定一个数字数组，我们需要使用二分搜索法搜索数组中 x 元素的存在。

示例:

```php
Input : 1 2 3 4 5
        5 
Output : 5 Exists

Input : 1 5 8
        0
Output : 0 Doesnt Exist

```

这种搜索技术比线性搜索更有效。

**方法 1(迭代)**:

涉及的步骤:
1)对数组进行排序，因为二分搜索法只在排序的范围内工作
2)如果我们要搜索的元素大于右侧的中间元素搜索，则计算中间元素，否则在左侧搜索。
3)如果找到元素，返回真。

```php
<?php

function binarySearch(Array $arr, $x)
{
    // check for empty array
    if (count($arr) === 0) return false;
    $low = 0;
    $high = count($arr) - 1;

    while ($low <= $high) {

        // compute middle index
        $mid = floor(($low + $high) / 2);

        // element found at mid
        if($arr[$mid] == $x) {
            return true;
        }

        if ($x < $arr[$mid]) {
            // search the left side of the array
            $high = $mid -1;
        }
        else {
            // search the right side of the array
            $low = $mid + 1;
        }
    }

    // If we reach here element x doesnt exist
    return false;
}

// Driver code
$arr = array(1, 2, 3, 4, 5);
$value = 5;
if(binarySearch($arr, $value) == true) {
    echo $value." Exists";
}
else {
    echo $value." Doesnt Exist";
}
?>
```

输出:

```php
5 Exists

```

**方法 2(递归):**
递归是一种我们重复调用同一个函数，直到一个基本条件匹配结束递归的方法。
继续方法 1 中的步骤，我们使用相同的思想，只是以递归方式改变函数的参数，并分解问题。

```php
function binarySearch(Array $arr, $start, $end, $x){
    if ($end < $start)
        return false;

    $mid = floor(($end + $start)/2);
    if ($arr[$mid] == $x) 
        return true;

    elseif ($arr[$mid] > $x) {

        // call binarySearch on [start, mid - 1]
        return binarySearch($arr, $start, $mid - 1, $x);
    }
    else {

        // call binarySearch on [mid + 1, end]
        return binarySearch($arr, $mid + 1, $end, $x);
    }
}

// Driver code
$arr = array(1, 2, 3, 4, 5);
$value = 5;
if(binarySearch($arr, 0, count($arr) - 1, $value) == true) {
    echo $value." Exists";
}
else {
    echo $value." Doesnt Exist";
}
```

输出:

```php
5 Exists

```

**相关 PHP 函数:**
 [in_array()在 PHP 中](https://www.geeksforgeeks.org/php-in_array-function/)
T7】array _ key _ exists()在 PHP 中