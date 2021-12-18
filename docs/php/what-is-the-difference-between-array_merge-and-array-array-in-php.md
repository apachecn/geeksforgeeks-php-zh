# PHP 中 array_merge 和 array + array 有什么区别？

> 原文:[https://www . geesforgeks . org/array _ merge-and-array-in-PHP/](https://www.geeksforgeeks.org/what-is-the-difference-between-array_merge-and-array-array-in-php/)区别是什么

在 PHP 中，数组可以使用数组并集(+)运算符或使用 array_merge()函数来连接。这两种方法有细微的差别。array_merge()函数是一个内置函数，用于连接两个数组，而不考虑它们的类型(数字、分类等)。)
**array_merge()函数:**array _ merge()合并一个或多个作为输入提供的数组，并提供一个新数组作为输出。在这个合并过程中，数组的值被附加到前一个数组的末尾，以生成结果数组。
**语法:**

```php
array array_merge( $arr1, $arr2, $arr3... )
```

**参数:**array _ merge()函数接受一个或多个输入数组，并将它们合并成一个结果数组。
**注意:**在 array_merge()函数中，如果输入数组具有相同的字符串键(在分类数组的情况下)，那么在结果数组中，键的后一个值将覆盖前一个值。但是如果数组包含数字键(在数字数组的情况下)，那么这些值不会被替换，它们只是被追加到结果数组中。同样，对于数字数组，键值将在结果数组中从零开始重新编号。
**数组并集(+)运算符:**合并两个数组的另一种方法是数组并集(+)运算符。这是一个二进制运算符，意味着它一次合并两个数组。union 运算符将右手数组追加到左手数组的末尾。
**语法:**

```php
$arr3 = $arr1 + $arr2
```

**参数:**union(+)运算符一次处理两个数组，并生成结果数组。
**注意:**在数组并集(+)运算符的情况下，两个数组中相同的键对应于左侧数组中的键的值将被取入结果数组中。同样，在数值数组的情况下，右手数组与左手数组的索引将在结果数组中被忽略。
**程序:**解释 array_merge()和 array union(+)区别的 PHP 代码。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Merge two arrays where one key ('one') is same

$arr1 = array( 'zero' => 0,
               'one' => 1,
               'two' => 2, 10, 11, 12, 13
        );

$arr2 = array( 'one' => 11,
               'three' => 3,
               'four' => 4, 12, 13, 14, 15
        );

// Merging both array using array_merge() function

// Here in $arr3 the value corresponding to
// the key 'one' will be from $arr2 and
// numeric keys will be renumbered

$arr3 = array_merge($arr1, $arr2);

echo "Result of array_merge() function\n";

print_r($arr3);

// Merging both array using array union(+) operator
// Here in $arr4 the value corresponding to the key
// 'one' will be from $arr1 and numeric keys
// which are repeated in $arr2 will be ignored

$arr4 = $arr1 + $arr2;

echo "\nResult of array union(+) operator\n";

print_r($arr4);

?>
```

**Output**

```php
Result of array_merge() function
Array
(
    [zero] => 0
    [one] => 11
    [two] => 2
    [0] => 10
    [1] => 11
    [2] => 12
    [3] => 13
    [three] => 3
    [four] => 4
    [4] => 12
    [5] => 13
    [6] => 14
    [7] => 15
)

Result of array union(+) operator
Array
(
    [zero] => 0
    [one] => 1
    [two] => 2
    [0] => 10
    [1] => 11
    [2] => 12
    [3] => 13
    [three] => 3
    [four] => 4
)

```