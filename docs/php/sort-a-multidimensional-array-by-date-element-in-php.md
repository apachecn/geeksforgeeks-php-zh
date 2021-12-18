# 在 PHP 中按日期元素对多维数组进行排序

> 原文:[https://www . geesforgeks . org/sort-a-多维数组-按日期排列-php 中的元素/](https://www.geeksforgeeks.org/sort-a-multidimensional-array-by-date-element-in-php/)

按包含日期的元素对多维数组进行排序。使用 [usort()](https://www.geeksforgeeks.org/php-usort-function/) 函数对数组进行排序。usort()函数是一个 PHP 内置函数，使用用户定义的比较函数对给定的数组进行排序。该函数将新的整数键从零开始赋给数组元素。

**语法:**

```
boolean usort( $array, "function_name")
```

**参数:**该函数接受两个参数，如上面的语法所示，描述如下:

*   **$array:** 此参数指定要排序的数组。
*   **function_name:** 此参数指定用户定义函数的名称，该函数比较参数$array 指定的值并对数组进行排序。该函数根据以下条件返回一个整数值。如果两个参数相等，则返回 0；如果第一个参数大于第二个参数，则返回 1；如果第一个参数小于第二个参数，则返回-1。

**返回值:**该函数返回布尔类型值。成功时返回真，失败时返回假。

我们使用 [strtotime](https://www.geeksforgeeks.org/php-strtotime-function/) 将给定的时间字符串转换为时间戳对象。一旦我们有了时间戳，我们就减去它们来决定更大的时间戳。

**程序:**

```
<?php

// Declare a multidimensional array
// and initialize it
$array = Array (
    Array (
        "gfg" => "GFG_1",
        "datetime" => "2019-02-22 11:29:45",
        ),
    Array (
        "gfg" => "GFG_2",
        "datetime" => "2019-02-13 11:29:45",
    ),
    Array (
        "gfg" => "GFG_3",
        "datetime" => "2019-02-15 11:29:45",
    )
);

// Comparison function
function date_compare($element1, $element2) {
    $datetime1 = strtotime($element1['datetime']);
    $datetime2 = strtotime($element2['datetime']);
    return $datetime1 - $datetime2;
} 

// Sort the array 
usort($array, 'date_compare');

// Print the array
print_r($array)

?>
```

**Output:**

```
Array
(
    [0] => Array
        (
            [gfg] => GFG_2
            [datetime] => 2019-02-13 11:29:45
        )

    [1] => Array
        (
            [gfg] => GFG_3
            [datetime] => 2019-02-15 11:29:45
        )

    [2] => Array
        (
            [gfg] => GFG_1
            [datetime] => 2019-02-22 11:29:45
        )

)

```