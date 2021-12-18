# 如何用 PHP 中的 stdClass()将数组转换成对象？

> 原文:[https://www . geesforgeks . org/如何使用 php 中的 stdclass 将数组转换为对象/](https://www.geeksforgeeks.org/how-to-convert-an-array-into-object-using-stdclass-in-php/)

要将数组转换为对象，需要使用[**【stdClass()**](https://www.geeksforgeeks.org/what-is-stdclass-in-php/)。stdClass()是一个空类，用于将其他类型强制转换为对象。如果一个对象被转换为对象，它不会被修改。但是，如果对象类型被转换/类型转换，则创建一个 stdClass 的实例，如果它不为空。如果为空，新实例将为空。

**示例 1:** 它使用 stdClass 将数组转换为对象。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Function to convert array into
// stdClass object
function ToObject($Array) {

    // Create new stdClass object
    $object = new stdClass();

    // Use loop to convert array into
    // stdClass object
    foreach ($Array as $key => $value) {
        if (is_array($value)) {
            $value = ToObject($value);
        }
        $object->$key = $value;
    }
    return $object;
}

// Declare an array and initialize it
$Original = array (
    '1' => array(
        'sNo' => '1',
        'Age' => '20',
        'name' => 'A'
    ),
    '2' => array(
        'sNo' => '2',
        'Age' => '21',
        'name' => 'B'
    ),
    '3' => array(
        'sNo' => '3',
        'Age' => '22',
        'name' => 'C'
    ),
    '4' => array(
        'sNo' => '4',
        'Age' => '23',
        'name' => 'D'
    ),
    '5' => array(
        'sNo' => '5',
        'Age' => '24',
        'name' => 'E'
    )
);

// Display the original array
print_r($Original);

// Function call
$convertedObj = ToObject($Original);

// Display the stdClass object
print_r($convertedObj);

?>
```

**Output:** 

```php
Array
(
    [1] => Array
        (
            [sNo] => 1
            [Age] => 20
            [name] => A
        )

    [2] => Array
        (
            [sNo] => 2
            [Age] => 21
            [name] => B
        )

    [3] => Array
        (
            [sNo] => 3
            [Age] => 22
            [name] => C
        )

    [4] => Array
        (
            [sNo] => 4
            [Age] => 23
            [name] => D
        )

    [5] => Array
        (
            [sNo] => 5
            [Age] => 24
            [name] => E
        )

)
stdClass Object
(
    [1] => stdClass Object
        (
            [sNo] => 1
            [Age] => 20
            [name] => A
        )

    [2] => stdClass Object
        (
            [sNo] => 2
            [Age] => 21
            [name] => B
        )

    [3] => stdClass Object
        (
            [sNo] => 3
            [Age] => 22
            [name] => C
        )

    [4] => stdClass Object
        (
            [sNo] => 4
            [Age] => 23
            [name] => D
        )

    [5] => stdClass Object
        (
            [sNo] => 5
            [Age] => 24
            [name] => E
        )

)
```

**示例 2:** 它使用 stdClass 将数组转换为对象。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Function to convert array into
// stdClass object
function ToObject($Array) {

    // Create new stdClass object
    $object = new stdClass();

    // Use loop to convert array into object
    foreach ($Array as $key => $value) {
        if (is_array($value)) {
            $value = ToObject($value);
        }
        $object->$key = $value;
    }
    return $object;
}

// Declare an array
$Original = array(1, 2, 3, 4, 5, 6);

// Display the array element
print_r($Original);

// Function call to convert object
$convertedObj = ToObject($Original);

// Display the stdClass object
print_r($convertedObj);

?>
```

**Output:** 

```php
Array
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
    [5] => 6
)
stdClass Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
    [5] => 6
)
```