# 在 PHP 中按对象字段对对象数组进行排序

> 原文:[https://www . geesforgeks . org/sort-objects-array-by-object-field-in-PHP/](https://www.geeksforgeeks.org/sort-array-of-objects-by-object-fields-in-php/)

给定一个对象数组，任务是按给定的字段按对象对数组进行排序。

**方法:**
[usort()](https://www.geeksforgeeks.org/php-usort-function/)函数是 PHP 中的一个内置函数，用于使用给定的比较器函数有条件地对元素数组进行排序。usort()函数也可用于按对象字段对对象数组进行排序。调用 usort()函数，将第一个参数作为对象数组，将第二个参数作为比较器函数，在此基础上对两个数组对象进行比较。

**示例:**

```
<?php

// PHP program to show sorting of 
// array of objects by object fields

// School Data array
$gfg_array = array(
    array(
        'score' => '100',
        'name' => 'Sam',
        'subject' => 'Data Structures'
    ),
    array(
        'score' => '50',
        'name' => 'Tanya',
        'subject' => 'Advanced Algorithms'
    ),
    array(
        'score' => '75',
        'name' => 'Jack',
        'subject' => 'Distributed Computing'
    )
);

// Class for encapsulating school data
class geekSchool {

    var $score, $name, $subject;

    // Constructor for class initialization
    public function geekSchool($data) {
        $this->name = $data['name'];
        $this->score = $data['score'];
        $this->subject = $data['subject'];
    }
}

// Function to convert array data to class object
function data2Object($data) {
    $class_object = new geekSchool($data);
    return $class_object;
}

// Comparator function used for comparator
// scores of two object/students
function comparator($object1, $object2) {
    return $object1->score > $object2->score;
}

// Generating array of objects
$school_data = array_map('data2Object', $gfg_array);

// Printing original object array data
print("Original object array:\n");

print_r($school_data);

// Sorting the class objects according 
// to their scores
usort($school_data, 'comparator');

// Printing sorted object array data
print("\nSorted object array:\n");

print_r($school_data);

?>
```

**Output:**

```
Original object array:
Array
(
    [0] => geekSchool Object
        (
            [score] => 100
            [name] => Sam
            [subject] => Data Structures
        )

    [1] => geekSchool Object
        (
            [score] => 50
            [name] => Tanya
            [subject] => Advanced Algorithms
        )

    [2] => geekSchool Object
        (
            [score] => 75
            [name] => Jack
            [subject] => Distributed Computing
        )

)

Sorted object array:
Array
(
    [0] => geekSchool Object
        (
            [score] => 50
            [name] => Tanya
            [subject] => Advanced Algorithms
        )

    [1] => geekSchool Object
        (
            [score] => 75
            [name] => Jack
            [subject] => Distributed Computing
        )

    [2] => geekSchool Object
        (
            [score] => 100
            [name] => Sam
            [subject] => Data Structures
        )

)

```