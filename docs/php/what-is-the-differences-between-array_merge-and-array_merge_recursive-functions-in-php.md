# PHP 中 array_merge()和 array_merge_recursive()函数有什么区别？

> 原文:[https://www . geeksforgeeks . org/array _ merge-and-array _ merge-recursive-functions-in-PHP/](https://www.geeksforgeeks.org/what-is-the-differences-between-array_merge-and-array_merge_recursive-functions-in-php/)

**PHP array_merge():**PHP 中的 array _ merge 函数是一种用于将一个或多个数组合并或组合成单个数组的函数。当它们是两个或两个以上的数组，每个数组有不同的键，并且我们想将它们显示为一个数组时，使用这个函数。这意味着，如果它们是两个数组，如数组 A 和数组 B，并且这两个数组的元素都没有相同的键，那么使用这个 array_merge 函数，我们可以将这两个数组组合起来，它将显示为 AB。您也可以为该函数分配一个数组。

**示例:**因此，在下面的代码中，我们用不同的键声明了两个不同的数组，并使用 array_merge()组合了它们

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
$a1=array("Mumbai","Nashik");
$a2=array("Nagpur","Pune");
print_r(array_merge($a1,$a2));
?>
```

**Output**

```
Array
(
    [0] => Mumbai
    [1] => Nashik
    [2] => Nagpur
    [3] => Pune
)
```

**PHP array_merge_recursive():**PHP 中的 array _ merge _ recursive()函数是一种用于将一个或多个数组合并或组合成单个数组的函数。当它们是两个或两个以上的数组，并且至少两个或两个以上的数组元素具有相同的键，并且我们希望将它们显示为一个数组时，使用该函数。这意味着，如果它们是作为数组 A 和数组 B 的两个数组，并且这两个数组的至少两个元素具有相同的键，那么使用这个 array_merge-recursive()函数，我们可以将这两个数组组合起来，它将显示为 AB。如果您只给这个函数分配了一个数组，那么它将与 array_merge()的作用相同。

**示例:**因此，在下面的代码中，我们声明了两个数组，其中两个元素具有相同的键，并使用 array_merge_recursive()成功地组合了它们。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
$a1=array("a"=>"Mumbai","b"=>"Nashik");
$a2=array("c"=>"Nagpur","b"=>"Pune");
print_r(array_merge_recursive($a1,$a2));
?>
```

**Output**

```
Array
(
    [a] => Mumbai
    [b] => Array
        (
            [0] => Nashik
            [1] => Pune
        )

     => Nagpur
)
```

**array _ merge()与 array_merge_recursive()的区别:**

<figure class="table">..);

| **array _ merge()** | **array _ merge _ recursive()** |
| --- | --- |
| This function is used to combine two or more arrays into a single array. | This function is used to combine multiple arrays so that the value of one array is appended to the end of the last array. |
| 语法:array_merge_recursive($array1，$array2，$array3…..); |

</figure>