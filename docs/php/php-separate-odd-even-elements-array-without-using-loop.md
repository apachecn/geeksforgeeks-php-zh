# PHP|不使用循环将奇偶元素与数组分开

> Original: [https://www.geeksforgeeks.org/php-separate-odd-even-elements-array-without-using-loop/](https://www.geeksforgeeks.org/php-separate-odd-even-elements-array-without-using-loop/)

在 PHP 中，您将看到一个由 n 个元素组成的数组。 您必须根据元素是奇数还是偶数将元素与数组分开。 也就是说，在不遍历原始数组或使用任何[循环](https://www.geeksforgeeks.org/php-loops/)的情况下，分别打印奇数组和偶数组。

例如：

```
Input : array(2, 5, 6, 3, 0)
Output : Odd array: 5 , 3
         Even array: 2, 6, 0

Input : $input = array(0, 1, 2, 3, 4, 5)
Output : Odd array: 1, 3, 5
         Even array: 0, 2, 4

```

这类问题可以通过遍历数组并分别打印奇数和偶数元素来轻松解决，但这会占用更多的代码行，并且还会增加代码中循环的开销。 因此，为了避免使用循环，我们将尝试使用 PHP 的一些内置函数。 这里我们使用两个 PHP 数组函数[ARRAY_FILTER()](https://www.geeksforgeeks.org/php-array_filter-function/)和[ARRAY_VALUES()](https://www.geeksforgeeks.org/php-array_values-function/)来解决这个问题。

*   **array_filter()：**此函数将用于过滤输入数组中的奇/偶元素。
*   **ARRAY_VALUES()：**当 ARRAY_FILTER 奇数组和偶数组与其元素在输入数组中的索引相同后，此函数将用于对奇数组和偶数组进行重新索引。

**注意：**ARRAY_FILTER()函数将只过滤奇数/偶数索引元素及其索引值。 应用 array_filter()函数后，奇数组的索引为 1、3、5，偶数组的索引为 0、2、4。

**算法：**

```
1.  过滤器元素：
    *   通过 array_filter()过滤奇数元素。
    *   根据 ARRAY_FILTER()过滤偶数元素。
    2.  重新索引数组：
    *   使用 ARRAY_VALUES()重新索引奇数组。
    *   使用 ARRAY_VALUES()重新索引偶数组。
    3.  同时打印奇数/偶数组。

```

以下是上述算法的 PHP 实现：

```
<?php

// PHP program to separate odd-even indexed
// elements of an array

// input array 
$input = array(4, 3, 6, 5, 8, 7, 2);

// comparator function to filter odd elements
function oddCmp($input)
{
    return ($input & 1);
}

// comparator function to filter odd elements
function evenCmp($input)
{
    return !($input & 1);
}

// filter odd-index elements
$odd = array_filter($input, "oddCmp");

// filter even-index elements
$even = array_filter($input, "evenCmp");

// re-index odd array by use of array_values()
$odd = array_values(array_filter($odd));

// re-index even array by use of array_values()
$even = array_values(array_filter($even));

// print odd-indexed array
print"Odd array :\n";
print_r($odd);

// print even-indexed array
print"\nEven array :\n";
print_r($even);

?>
```

发帖主题：Re：Kolibrios

```
Odd array :
Array
(
    [0] => 3
    [1] => 5
    [2] => 7
)

Even array :
Array
(
    [0] => 4
    [1] => 6
    [2] => 8
    [3] => 2
)

```