# 求数组

标准差的 PHP 程序

> Original: [https://www.geeksforgeeks.org/php-program-find-standard-deviation-array/](https://www.geeksforgeeks.org/php-program-find-standard-deviation-array/)

给定一个元素数组。 我们需要找到 PHP 中数组元素的[标准差](https://www.geeksforgeeks.org/mathematics-mean-variance-and-standard-deviation/)。

示例：

```php
Input : array(2, 3, 5, 6, 7)
Output : 1.5620499351813

Input : array(1, 2, 3, 4, 5)
Output : 1

```

使用[PHP](https://www.geeksforgeeks.org/php/)内置函数可以解决以下问题。 用于解决上述问题的内置函数如下：

1.  [ARRAY_SUM ()](https://www.geeksforgeeks.org/php-array_sum-function-2/) : this function returns the sum of all the elements in the array.
2.  [count ()](https://www.geeksforgeeks.org/php-count-function/) : this function gives the number of elements that currently exist in a given array.
3.  [sqrt ()](https://www.geeksforgeeks.org/php-sqrt-function/) : this function returns the square root of a given number.

要计算标准差，我们必须先计算方差。 方差可以计算为所有数字和平均值之间差异的平方和。 最后，为了获得标准差，我们将使用公式√(VARIANCE/NO_OF_ELEMENTS)。

以下是计算标准差的 PHP 实现：

```php
<?php

    // function to calculate the standard deviation
    // of array elements
    function Stand_Deviation($arr)
    {
        $num_of_elements = count($arr);

        $variance = 0.0;

                // calculating mean using array_sum() method
        $average = array_sum($arr)/$num_of_elements;

        foreach($arr as $i)
        {
            // sum of squares of differences between 
                        // all numbers and means.
            $variance += pow(($i - $average), 2);
        }

        return (float)sqrt($variance/$num_of_elements);
    }

    // Input array
    $arr = array(2, 3, 5, 6, 7);

    print_r(Stand_Deviation($arr));

?>
```

帖子主题：Re：Колибри