# PHP|数组中第二频繁的元素

> Original: [https://www.geeksforgeeks.org/php-second-frequent-element-array/](https://www.geeksforgeeks.org/php-second-frequent-element-array/)

给定一个数组，我们必须找到该数组中出现频率第二高的元素。

例如：

```php
Input : array(3, 3, 4, 5, 5, 5, 9, 8, 8, 8, 8, 8);
Output : Second most frequent element is: 5

Input : array("geeks", "for", "geeks");
Output : Second most frequent element is: for

```

在其他语言中，使用循环方法可以解决上述问题，但在 PHP 中，我们内置了执行此任务的函数。 具体功能如下：

*   **[ARRAY_COUNT_VALUES()](https://www.geeksforgeeks.org/php-array_count_values-function/)**：此函数用于计算所有元素的频率，并返回关联的数组，该数组包含值作为键，频率作为值。
*   **[arort()](https://www.geeksforgeeks.org/sorting-arrays-php-5/)**：此函数用于以逆序对元素进行排序，并维护关联的索引。
*   **[ARRAY_KEYS()](https://www.geeksforgeeks.org/php-array_keys-function/)**：此函数返回包含所有键或子集的数组。

**方法：**首先，我们使用**array_count_values**创建一个新的数组，其中包含以值为键的所有元素的频率，并将计数作为值。
使用**arort**对新数组进行逆序排序，然后使用**array_keys**获取已排序数组的所有键。 第二个键将是原始数组中第二频繁的元素。

下面是上述方法的说明：
**示例 1：**

```php
<?php    

    $arr = array(2, 2, 3, 4, 4, 4, 8, 8, 6, 6, 9, 9, 9, 9);

    // new array containing frequency of values of $arr
    $arr_freq = array_count_values($arr);    

     // arranging the new $arr_freq in decreasing order 
     // of occurrences
     arsort($arr_freq);

     // $new_arr containing the keys of sorted array
     $new_arr = array_keys($arr_freq);

     // Second most frequent element
     echo "Second most frequent element is:"." ".$new_arr[1];
?>
```

**Output:**

```php
Second most frequent element is: 4

```

**示例 2：**

```php
<?php

    $arr = array("Geeks", "for", "Geeks");

    // new array containing frequency of values of $arr
    $arr_freq = array_count_values($arr);

    // arranging the new $arr_freq in decreasing 
    // order of occurrences
    arsort($arr_freq);

    // $new_arr containing the keys of sorted array
    $new_arr = array_keys($arr_freq);

    // Second most frequent element
    echo "Second most frequent string is:"." ".$new_arr[1];
?>
```

**Output:**

```php
Second most frequent string is: for

```