# 如何在 PHP 数组中按多个键= >值进行搜索？

> 原文:[https://www . geesforgeks . org/如何通过 php 数组中的多键值进行搜索/](https://www.geeksforgeeks.org/how-to-search-by-multiple-key-value-in-php-array/)

在多维数组中，如果没有唯一的键= >值对(存在多个键= >值对)，那么在这种情况下，如果我们通过单个键= >值对搜索元素，那么它可以返回多个项目。因此，我们可以使用多个键= >值对来实现搜索，以获得唯一的项目。

**方法:**对于数组中的每个数组，迭代搜索数组，如果任何搜索键值与对应的数组键值不匹配，我们将丢弃该数组，并继续下一个数组的过程。让我们通过一个例子来更好地理解这一点:
假设我们想要从包含不同部分的学生的学生列表中搜索学生详细信息，因此，在这种情况下，仅使用 rollNo 可能无法给出正确的输出。所以我们需要用两个键= >值搜索列表，即 rollNO 和 section。

**示例:**

```php
<?php

// PHP program to search for multiple
// key=>value pairs in array

function search($array, $search_list) {

    // Create the result array
    $result = array();

    // Iterate over each array element
    foreach ($array as $key => $value) {

        // Iterate over each search condition
        foreach ($search_list as $k => $v) {

            // If the array element does not meet
            // the search condition then continue
            // to the next element
            if (!isset($value[$k]) || $value[$k] != $v)
            {

                // Skip two loops
                continue 2;
            }
        }

        // Append array element's key to the
        //result array
        $result[] = $value;
    }

    // Return result 
    return $result;
}

// Multidimensional array for students list
$arr = array(
    1 => array(
        'rollNo' => 44,
        'name' => 'Alice',
        'section' => 'B'
    ),
    2 => array(
        'rollNo' => 3,
        'name' => 'Amit',
        'section' => 'B'
    ),
    3 => array(
        'rollNo' => 3,
        'name' => 'Bob',
        'section' => 'A'
    ),
    4 => array(
        'rollNo' => 5,
        'name' => 'Gaurav',
        'section' => 'B'
    ),
    5 => array(
        'rollNo' => 5,
        'name' => 'Gaurav',
        'section' => 'A'
    ) 
);

// Define search list with multiple key=>value pair
$search_items = array('rollNo'=>5, 'section'=>"A");

// Call search and pass the array and
// the search list
$res = search($arr, $search_items);

// Print search result
foreach ($res as $var) {
    echo 'RollNo: ' . $var['rollNo'] . '<br>';
    echo 'Name: ' . $var['name'] . '<br>';
    echo 'Section: ' . $var['section'] . '<br>';        
}

?>
```

**Output:**

```php
RollNo: 5
Name: Gaurav
Section: A

```