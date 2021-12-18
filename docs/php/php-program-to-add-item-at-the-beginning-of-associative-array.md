# 在关联数组

开头添加项的 PHP 程序

> Original: [https://www.geeksforgeeks.org/php-program-to-add-item-at-the-beginning-of-associative-array/](https://www.geeksforgeeks.org/php-program-to-add-item-at-the-beginning-of-associative-array/)

在 PHP 中，关联数组是索引不需要像索引数组那样严格连续的数组类型。 通常，在现有的关联数组中添加一个新元素，该元素将被追加到该数组的末尾。

**示例：**

```
<?php

// Existing array
$arr = array('one' => 1, 'two' => 2);

// New element
$arr['zero'] = 0;

// Final array
print_r($arr);

?>
```

**Output:**

```
Array
(
    [one] => 1
    [two] => 2
    [zero] => 0
)

```

因此，新元素不能直接添加到关联数组的开头，但现有数组可以附加到新数组的末尾，其中第一个元素是新元素。
意思是先在开头添加新元素，新元素需要放入一个空数组中作为第一个元素，然后将该数组与已有数组合并。 在 PHP 中，有两种合并数组的方法，一种是 array_merge()函数，另一种是使用数组并集(+)运算符。

在*ARRAY_MERGE()函数*的情况下，如果两个数组具有相同的键，则在结果数组中考虑与后面数组中的键相对应的值。 但在索引数组的情况下，只需追加元素，并对结果数组中的所有元素进行重新索引。

**语法：**

```
*array* array_merge( $arr1, $arr2 )
```

在*数组并集(+)运算符*的情况下，如果两个数组具有相同的键，则在结果数组中考虑与第一个数组中的键相对应的值，这也适用于索引数组，如果两个数组具有公共索引的元素，则结果数组中将只考虑第一个数组中的元素。

**语法：**

```
$arr3 = $arr1 + $arr2
```

**程序：**在关联数组开头添加新项的 PHP 程序。

```
<?php

// Adding a new element at the beginning of an array

// Existing array
$arr = array('one' => 1, 'two' => 2, 'three' => 3);

// New element to be added at 'zero' => 0

// Create an array using the new element
$temp = array('zero' => 0);

// Append the $temp in the beginning of $arr

// Using array union(+) operator
$arr2 = $temp + $arr;

echo "Result of array union(+) : ";
print_r($arr2);

// Using array_merge() function
$arr3 = array_merge($temp, $arr);

echo "\n" . "Result of array_merge() : ";
print_r($arr3);

?>
```

**Output:**

```
Result of array union(+) : Array
(
    [zero] => 0
    [one] => 1
    [two] => 2
    [three] => 3
)

Result of array_merge() : Array
(
    [zero] => 0
    [one] => 1
    [two] => 2
    [three] => 3
)

```