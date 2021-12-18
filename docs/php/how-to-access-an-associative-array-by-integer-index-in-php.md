# PHP 中如何通过整数索引访问关联数组？

> 原文:[https://www . geesforgeks . org/如何访问 php 中的整数索引关联数组/](https://www.geeksforgeeks.org/how-to-access-an-associative-array-by-integer-index-in-php/)

PHP 中有两种类型的数组，索引数组和关联数组。如果是索引数组，则遵循严格的数字索引，但是如果是关联数组，则有对应于每个元素的键。
关联数组的元素只能通过对应的键来访问。因为键之间没有严格的索引，所以在 PHP 中通常通过整数索引访问元素是不可能的。

虽然 *array_keys()函数*可用于获取关联数组的索引键数组。当结果数组被索引时，结果数组的元素可以通过整数索引来访问。使用这个结果数组，原始数组的键可以通过整数索引来访问，然后这些键可以用来访问原始数组的元素。因此，通过使用整数索引，可以在额外的索引键数组的帮助下访问原始数组的元素。

**array_keys()函数:**array _ keys()函数将一个数组作为输入，返回一个只由原始数组的键组成的索引数组，索引从零开始。

**语法:**

```
array array_keys( $arr )
```

**参数:**array _ keys()函数将一个数组作为输入，只使用该数组的键来构成索引的结果数组。

**注意:**array _ keys()函数不改变原数组的键的顺序。如果传递了一个索引数组，那么得到的数组将以整数作为值。

**程序:**使用整数索引访问关联数组的 PHP 程序。

```
<?php
// PHP program to accessing an associative
// array by integer index

// Sample associative array
$arr = array( 'one' => 'geeks',
              'two' => 'for', 
              'three' => 'geeks'
        );

// Getting the keys of $arr
// using array_keys() function
$keys = array_keys( $arr );

echo "The keys array: ";

print_r($keys);

// Getting the size of the sample array
$size = sizeof($arr);

//Accessing elements of $arr using
//integer index using $x
echo "The elements of the sample array: " . "\n";

for($x = 0; $x < $size; $x++ ) {
    echo "key: ". $keys[$x] . ", value: " 
            . $arr[$keys[$x]] . "\n";
}

?>
```

**Output:**

```
The keys array: Array
(
    [0] => one
    [1] => two
    [2] => three
)
The elements of the sample array: 
key: one, value: geeks
key: two, value: for
key: three, value: geeks

```