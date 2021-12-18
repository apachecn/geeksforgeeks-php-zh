# 用 PHP 重置数组元素的键？

> 原文:[https://www . geesforgeks . org/reset-key-of-array-elements-using-PHP/](https://www.geeksforgeeks.org/reset-keys-of-array-elements-using-php/)

在 PHP 中，两种类型的数组是可能的索引数组和关联数组。在索引数组的情况下，元素是严格的整数索引，在关联数组的情况下，每个元素都有相应的键与之相关联，并且只能使用这些键来访问元素。

要使用整数索引访问关联数组的键和值，可以使用 *array_keys()* 和 *array_values()* 内置函数。

*   **array_keys()** 函数接受一个数组的输入，并从输入数组中返回唯一键的索引数组。
*   **array_values()** 函数接受一个数组的输入，并从输入数组返回只包含值的索引数组。

现在，要重置数组元素的键，可以执行两个操作，*键 _ 交换()*和*键 _ 改变()*。因为这些不是内置函数，所以必须在代码中实现。

**使用 key_swap()函数:**该函数将取输入一个数组和两个键，然后借助另一个变量($val)交换这两个键对应的值，并返回结果数组。

**注意:**如果两个键都不在数组中，这个函数会抛出一个错误。

**使用 key_change()函数:**该函数将输入一个数组和两个键，一个旧键(已经存在于数组中)和一个新键。该函数首先将旧键对应的值存储到第三个变量($val)中，然后从数组中删除(unset())旧键及其对应的值。然后，新的键将被添加到数组中，存储在第三个变量($val)中的值将被分配给它，结果数组将被返回。

**注意:**如果新键不在数组中，该函数将返回所需的输出，否则如果新键出现在输入数组中，新键的值将丢失，因为旧键的值将覆盖它。此外，如果输入数组中没有旧键，函数将抛出一个错误。

**程序:** PHP 程序重置数组中数组元素的键。

```php
<?php
// PHP program to reset the keys of array elements

// Function to swap the values of any
// two keys in an array 
function key_swap($arr, $key1, $key2) {
    $val = $arr[$key1];
    $arr[$key1] = $arr[$key2];
    $arr[$key2] = $val;
    return $arr;
}

// Function to change the key corresponding
// to the value in an array
function key_change($arr, $oldkey, $newkey){
    $val = $arr[$oldkey];
    unset($arr[$oldkey]);
    $arr[$newkey] = $val;
    return $arr;
}

// Sample associative array
$arr = array( 'zero' => 1,
              'one' => 2,
              'two' => 0,
              'test' => 3
        );

// Print the sample array
echo "The Sample array: ";
print_r($arr);

// Swap the keys 'zero' and 'one'
$arr = key_swap($arr, 'zero', 'one');

// Swap the keys 'zero' and 'two'
$arr = key_swap($arr, 'zero', 'two');

// Change the key 'test' to 'three'
$arr = key_change($arr, 'test', 'three');

// Print the modified array
echo "The Modified array: ";
print_r($arr);

?>
```

**Output:**

```php
The Sample array: Array
(
    [zero] => 1
    [one] => 2
    [two] => 0
    [test] => 3
)
The Modified array: Array
(
    [zero] => 0
    [one] => 1
    [two] => 2
    [three] => 3
)

```