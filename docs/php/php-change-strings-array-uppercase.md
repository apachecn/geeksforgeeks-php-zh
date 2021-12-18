# PHP |将数组中的字符串改为大写

> 原文:[https://www . geesforgeks . org/PHP-change-strings-array-大写/](https://www.geeksforgeeks.org/php-change-strings-array-uppercase/)

给你一个字符串数组。您必须将给定数组中的所有字符串都更改为大写，无论它们当前是哪种情况。打印结果数组。

示例:

```php
Input : arr[] = ("geeks", "For", "GEEks")
Output : Array ([0]=>GEEKS [1]=>FOR [2]=>GEEKS)

Input :  arr[] = ("geeks")
Output : Array ([0]=>GEEKS)

```

要解决这个问题，一个基本的方法是迭代输入数组的所有字符串，然后将它们一个接一个地变成大写，并打印出来。数组迭代充分利用了程序中的 for 循环，这可以通过使用一些聪明的方法来避免，如[数组 _change_key_case()](https://www.geeksforgeeks.org/php-array_change_key_case-function/) 和[数组 _flip()](https://www.geeksforgeeks.org/php-array_flip-function/) 。我们要做的只是将数组键翻转为值，反之亦然，然后改变数组新键的大小写，这实际上改变了原始字符串值的大小写，然后再次通过 array_flip()翻转键和值。

下面是一步一步的过程:

1.  使用 [array_flip()](https://www.geeksforgeeks.org/php-array_flip-function/) 功能用数组中存在的值交换键。
    也就是说，这些键现在将变成值，它们各自的值将成为它们的新键。
2.  使用 [array_change_key_case()](https://www.geeksforgeeks.org/php-array_change_key_case-function/) 功能改变当前按键的大小写(原值)。
3.  再次使用 [array_flip()](https://www.geeksforgeeks.org/php-array_flip-function/) 函数翻转数组的键和值，得到字符串值大写的
    原始数组。

下面是上述方法在 PHP 中的实现:

```php
<?php

// Program to change strings in an array to upper case

$input = array("Practice", "ON", "GeeKs", "is best");

// print array before conversion of string
print"Array before string conversion:\n";
print_r($input);

// Step 1: flip array key => value
$input = array_flip($input);

// Step 2: change case of new keys to upper
$input = array_change_key_case($input, CASE_UPPER);

// Step 3: reverse the flip process to 
// regain strings as value
$input = array_flip($input);

// print array after conversion of string
print"\nArray after string conversion:\n";
print_r($input);

?>
```

输出:

```php
Array before string conversion:
Array
(
    [0] => Practice
    [1] => ON
    [2] => GeeKs
    [3] => is best
)

Array after string conversion:
Array
(
    [0] => PRACTICE
    [1] => ON
    [2] => GEEKS
    [3] => IS BEST
)

```