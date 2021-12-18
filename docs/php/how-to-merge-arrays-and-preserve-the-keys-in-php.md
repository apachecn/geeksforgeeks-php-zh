# PHP 中如何合并数组并保留密钥？

> 原文:[https://www . geeksforgeeks . org/如何合并数组并保留 php 中的密钥/](https://www.geeksforgeeks.org/how-to-merge-arrays-and-preserve-the-keys-in-php/)

[PHP 中的数组](https://www.geeksforgeeks.org/php-arrays/)是使用 array()函数创建的。数组是一次可以保存多个值的变量。有三种类型的阵列:

1.  索引数组
2.  关联数组
3.  多维数组

数组中的每个值都有一个附加的名称或标识，用于访问名为 key 的元素。

要合并两个数组 **array_merge()函数**工作正常，但不保留键。相反 **[array_replace()函数](https://www.geeksforgeeks.org/php-array_replace-function/)** 有助于合并两个数组，同时保留它们的键。

**程序 1:** 本示例使用 array_replace()函数合并两个数组并保留键。

```
<?php

// Create first associative array
$array1 = array(
    1 => 'Welcome',
    2 => 'To'
);

// Create second associative array
$array2 = array(
    3 => 'Geeks',
    4 => 'For',
    5 => 'Geeks'
);

// Use array_replace() function to
// merge the two array while
// preserving the keys
print_r(array_replace($array1, $array2));
?>
```

**Output:**

```
Array
(
    [1] => Welcome
    [2] => To
    [3] => Geeks
    [4] => For
    [5] => Geeks
)

```

**程序 1:** 本例使用 [array_replace_recursive()函数](https://www.geeksforgeeks.org/php-array_replace_recursive-function/)合并两个数组并保留键。

```
<?php

// Create first associative array
$array1 = array(
    1 => 'Welcome',
    2 => 'To'
);

// Create second associative array
$array2 = array(
    3 => 'Geeks',
    4 => 'For',
    5 => 'Geeks'
);

// Use array_replace() function to
// merge the two array while
// preserving the keys
print_r(array_replace_recursive($array1, $array2));
?>
```

**Output:**

```
Array
(
    [1] => Welcome
    [2] => To
    [3] => Geeks
    [4] => For
    [5] => Geeks
)

```