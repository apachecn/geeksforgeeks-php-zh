# 在 PHP 中如何在多维数组中通过 key= >值进行搜索？

> 原文:[https://www . geesforgeks . org/how-to-search-by-key value-in-多维数组-in-php/](https://www.geeksforgeeks.org/how-to-search-by-keyvalue-in-a-multidimensional-array-in-php/)

在 PHP 中，多维数组搜索是指在多级嵌套数组中搜索一个**键= >值**。这种搜索可以通过迭代或递归方法来完成。

**递归方法:**检查键是否存在于多维数组中，并且键的值是否等于所需的值，然后结果存储在数组中，并通过每个元素递归。

**示例:**在多维数组中搜索名字为“AMIT”的学生并打印结果的程序。

```
<?php
// PHP program to carry out multidimensional array
// search by key=>value

// Function to recursively search for a
// given key=>value 
function search($array, $key, $value) {
    $results = array();

    // if it is array
    if (is_array($array)) {

        // if array has required key and value
        // matched store result 
        if (isset($array[$key]) && $array[$key] == $value) {
            $results[] = $array;
        }

        // Iterate for each element in array
        foreach ($array as $subarray) {

            // recur through each element and append result 
            $results = array_merge($results, 
                    search($subarray, $key, $value));
        }
    }

    return $results;
}

// Multidimensional array for student list
$arr = array(
    "A" => array(
        1 => array('rollNo'=>101, 'name'=>"AMIT"),
        2 => array('rollNo'=>102, 'name'=>"BHUWAN"),
        3 => array('rollNo'=>103, 'name'=>"BOB"),
        4 => array('rollNo'=>104, 'name'=>"CAROT")
    ),
    "B" => array(
        1 => array('rollNo'=>201, 'name'=>"ABHISHEK"),
        2 => array('rollNo'=>202, 'name'=>"AMIT"),
        3 => array('rollNo'=>203, 'name'=>"RONNY"),
        4 => array('rollNo'=>204, 'name'=>"LOBO")
    ),
    "C" => array(
        1 => array('rollNo'=>301, 'name'=>"ANMOL"),
        2 => array('rollNo'=>302, 'name'=>"TONNY"),
        3 => array('rollNo'=>303, 'name'=>"SANJI")
    )
);

$res = search($arr, 'name', 'AMIT');

foreach ($res as $var) {
    echo $var["rollNo"]." - ".$var['name'] . "<br>";
}

?>
```

**Output:**

```
101 - AMIT
202 - AMIT

```

**迭代方法:**下面的实现是迭代方法

**示例:**程序以多维数组搜索住在“德里”的学生并打印结果。

```
<?php
// PHP program to carry out multidimensional
// array search by key=>value

// Function to iteratively search for a
// given key=>value  
function search($array, $key, $value) {

    // RecursiveArrayIterator to traverse an
    // unknown amount of sub arrays within
    // the outer array.
    $arrIt = new RecursiveArrayIterator($array);

    // RecursiveIteratorIterator used to iterate
    // through recursive iterators
    $it = new RecursiveIteratorIterator($arrIt);

    foreach ($it as $sub) {

        // Current active sub iterator
        $subArray = $it->getSubIterator();

        if ($subArray[$key] === $value) {
            $result[] = iterator_to_array($subArray);
         }
    }
    return $result;
}

// Multidimensional array for students list
$arr = array(
    "A" => array(
        1 => array('name'=>"Alice", 'location'=>"Dehradun"),
        2 => array('name'=>"BHUWAN", 'location'=>"Mumbai"),
        3 => array('name'=>"BOB", 'location'=>"Delhi"),
        4 => array('name'=>"CAROT", 'location'=>"Haryana")
    ),
    "B" => array(
        1 => array('name'=>"ABHISHEK", 'location'=>"Dehradun"),
        2 => array('name'=>"AMIT", 'location'=>"Delhi"),
        3 => array('name'=>"RONNY", 'location'=>"Bengaluru"),
        4 => array('name'=>"LOBO", 'location'=>"Pune")
    ),
    "C" => array(
        1 => array('name'=>"ANMOL", 'location'=>"Delhi"),
        2 => array('name'=>"TONNY", 'location'=>"Delhi"),
        3 => array('name'=>"SANJI", 'location'=>"Haryana")
    )
);

$res = search($arr, 'location', 'Delhi');

foreach ($res as $var) {
    echo $var["name"]." - ".$var['location'] ."<br>";
}

?>
```

**Output:**

```
BOB - Delhi
AMIT - Delhi
ANMOL - Delhi
TONNY - Delhi

```