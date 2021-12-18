# PHP 中如何统计所有数组元素？

> 原文:[https://www . geesforgeks . org/如何计算 php 中的所有数组元素/](https://www.geeksforgeeks.org/how-to-count-all-array-elements-in-php/)

我们给出了一个包含一些数组元素的数组，任务是使用 PHP 对数组 arr 的所有元素进行计数。为了完成这个任务，我们在 PHP 中有以下方法:

**方法 1:使用** [**计数()方法**](https://www.geeksforgeeks.org/php-count-function/)**:****计数()** 方法 用于计数数组中的当前元素。对于空数组，它返回 0。

**语法:**

```php
count($array, mode)

```

**示例:**

## PHP

```php
<?php
// PHP program to count all elements
// or values in an array

// Use of count() function
$array = array("Geek1", "Geek2",
            "Geek3", "1", "2","3");  

echo "Count first array elements: " . count($array) . "\n"; 

$array = array(
  'names' => array("Geek1", "Geek2", "Geek3"), 
  'rank' => array('1', '2', '3')
); 

echo "Recursive count: " . count($array, 1) . "\n"; 
echo "Normal count: " . count($array, 0); 

?>
```

**输出**

```php
Count first array elements: 6
Recursive count: 8
Normal count: 2 
```