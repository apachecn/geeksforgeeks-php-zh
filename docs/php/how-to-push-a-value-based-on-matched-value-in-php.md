# PHP 中如何推一个基于匹配值的值？

> 原文:[https://www . geeksforgeeks . org/如何在 php 中基于匹配值推送值/](https://www.geeksforgeeks.org/how-to-push-a-value-based-on-matched-value-in-php/)

在 PHP 中，为了在匹配时推进数组中的值，我们需要一个带有键和值对的数组。包含键和值对的数组称为[关联数组](https://www.geeksforgeeks.org/associative-arrays-in-php/)。

**方法:**创建两个不同的关联数组，命名为**数组 1** 和**数组 2** 。然后将数组 1 的值与数组 2 的键进行比较，如果我们得到匹配，那么我们将按如下方式推送静态键和值对:

**程序 1:**

```
<?php 

// Creating an associative array
$array1 = [
    "GFG1" => "1",
    "GFG2" => "2",
    "GFG3" => "3"
];

// Creating a multi-dimensional
// associative array
$array2 = [
    "1" => ["Subject" => "HTML"],
    "2" => ["Subject" => "CSS"],
    "3" => ["Subject" => "JavaScript"]
];

// Nested foreach loop to compare
// array1 and array2 elements
foreach( $array1 as $key1 => $value1 ) {

    foreach( $array2 as $key2 => $value2 ) {

        // Compare the key of array2 with
        // the value of array1
        if ($key2 == $value1) {

            // If a match is found then push
            // the element in array2 based
            // on the key
            $array2[$value1]["Organization"]
                        = "GeeksforGeeks";
        }
    }
}

// Display the array elements
print_r($array2);

?>
```

**Output:**

```
Array
(
    [1] => Array
        (
            [Subject] => HTML
            [Organization] => GeeksforGeeks
        )

    [2] => Array
        (
            [Subject] => CSS
            [Organization] => GeeksforGeeks
        )

    [3] => Array
        (
            [Subject] => JavaScript
            [Organization] => GeeksforGeeks
        )

)

```

在上面的程序中，该值被推入一个现有的数组中。如果你想在一个全新的数组中推送值，那么请看下面的程序。
**节目 2:**

```
<?php 

// Creating an associative array
$array1 = [
    "GFG1" => "1",
    "GFG2" => "2",
    "GFG3" => "3"
];

// Creating a multi-dimensional
// associative array
$array2 = [
    "1" => ["Subject" => "HTML"],
    "2" => ["Subject" => "CSS"],
    "3" => ["Subject" => "JavaScript"]
];

// Create an empty array
$array3 = [];

// Nested foreach loop to compare
// array1 and array2 elements
foreach( $array1 as $key1 => $value1 ) {

    foreach( $array2 as $key2 => $value2 ) {

        // Compare the key of array2 with
        // the value of array1
        if ($key2 == $value1) {

            // If a match is found then push
            // the array element into array3
            // based on the key
            $array3[$value1] = $array2[$value1];
        }
    }
}

// Display the array elements
print_r($array3);

?>
```

**Output:**

```
Array
(
    [1] => Array
        (
            [Subject] => HTML
        )

    [2] => Array
        (
            [Subject] => CSS
        )

    [3] => Array
        (
            [Subject] => JavaScript
        )

)

```

上述程序会将数组 2 中的值推送到数组 3 中，数组 3 为空。

**程序 3:**

```
<?php 

// Create an associative array
$department = [
    "dept1" => "IT",
    "dept2" => "CE",
    "dept3" => "CS",
    "dept4" => "EC"
];

// Create a multi-dimensional associative array
$student = [
    "IT" => ["total_students" => "60"],
    "CE" => ["total_students" => "65"],
    "CS" => ["total_students" => "62"]
];

// Nested foreach loop to compare
// $department and $student elements
foreach ($department as $dept => $d) {
    foreach ($student as $std => $s) {

        // Compare the key of $student array with
        // the value of $department array
        if ($std == $d) {
            $student[$d]["HOD"] = "XYZ";
        }
    }
}

// Display the array elements
print_r($student);

?>
```

**Output:**

```
Array
(
    [IT] => Array
        (
            [total_students] => 60
            [HOD] => XYZ
        )

    [CE] => Array
        (
            [total_students] => 65
            [HOD] => XYZ
        )

    [CS] => Array
        (
            [total_students] => 62
            [HOD] => XYZ
        )

)

```

在上面的程序中，学生数组中没有 dept4 的匹配项，因此它不会显示在输出部分。