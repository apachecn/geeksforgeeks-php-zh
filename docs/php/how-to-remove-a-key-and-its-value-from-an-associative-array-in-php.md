# 如何在 PHP 中从关联数组中移除一个键及其值？

> 原文:[https://www . geesforgeks . org/如何从 php 关联数组中移除键及其值/](https://www.geeksforgeeks.org/how-to-remove-a-key-and-its-value-from-an-associative-array-in-php/)

给定一个包含数组元素的关联数组，任务是从关联数组中移除一个键及其值。

**示例:**

```php
Input : array( "name" => "Anand", "roll"=> "1")
Output : Array (
    [roll] => 1
)

Input : array( "1" => "Add", "2" => "Multiply", "3" => "Divide")
Output : Array (
    [2] => Multiply
    [3] => Divide
)

```

**方法 1:使用 [unset()函数](https://www.geeksforgeeks.org/php-unset-function/):**unset()函数用于在关联数组中取消键及其值的设置。

**语法:**

```php
*void* unset( $array_name['key_to_be_removed'] )
```

**程序:**

```php
<?php

// Declare an associative array
$arr = array( 
    "1" => "Add",
    "2" => "Multiply",
    "3" => "Divide"
);

// Remove the key 1 and its value
// from associative array
unset($arr['1']);

// Display the array elements
print_r($arr);

?>
```

**Output:**

```php
Array
(
    [2] => Multiply
    [3] => Divide
)

```

**方法二:使用 [array_diff_key()函数](https://www.geeksforgeeks.org/php-array_diff_key-function/) :** 该函数用于获取一个或多个数组之间的差异。此函数比较一个或多个数组之间的键，并返回它们之间的差异。

**语法:**

```php
*array* array_diff_key( $array_name, array_flip((array) ['keys_to_be_removed'] )
```

**程序:**

```php
<?php

// Declare an associative array
$arr = array( 
    "1" => "a",
    "2" => "b",
    "3" => "c"
);

// Remove the key 1 and its value
// from associative array
$result = array_diff_key($arr, 
            array_flip((array) ['1']));

// Display the result
print_r($result);

?>
```

**Output:**

```php
Array
(
    [2] => b
    [3] => c
)

```