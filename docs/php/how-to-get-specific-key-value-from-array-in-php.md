# PHP 中如何从数组中获取特定键值？

> 原文:[https://www . geesforgeks . org/如何从 php 数组中获取特定键值/](https://www.geeksforgeeks.org/how-to-get-specific-key-value-from-array-in-php/)

在本文中，我们将看到如何从给定的数组中获取特定的键值。PHP 数组是存储在键下的项的集合。有两种可能的键类型:**字符串**和**整数**。对于任何类型的键，都有一种通过键获得特定值的通用语法——方括号。

**例 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$mixedArr = [
    10,
    20,
    'hello' => 'world',
    30,
];

// Get a specific value by index
$firstItem = $mixedArr[0];
echo "An item by index 0: {$firstItem}\n";

// Get a specific value by string key
$stringItem = $mixedArr['hello'];
echo "An item by key 'hello': {$stringItem}\n";

?>
```

**Output**

```php
An item by index 0: 10
An item by key 'hello': world
```

**例 2:** 有时候我们会不小心尝试从数组中获取一个不存在的项。在这种情况下，PHP 会抛出一个 NOTICE。为了避免这个问题，我们必须在访问密钥之前检查它是否存在。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$arr = [1, 2, 3];

// Check the key existence with 
// the built-in 'isset' function
if (isset($arr[10])) {
    echo "index 10 value is: {$arr[10]}\n";
} else {
    echo "There are no value under the index 10\n";
}

$value = $arr[10] ?? 'unknown';

echo "A value under the index 10: {$value}\n";

?>
```

**Output**

```php
There are no value under the index 10
A value under the index 10: unknown
```