# 如何在 PHP 中打印一个数组的所有值？

> 原文:[https://www . geesforgeks . org/如何打印 php 中数组的所有值/](https://www.geeksforgeeks.org/how-to-print-all-the-values-of-an-array-in-php/)

我们给出了一个包含一些数组元素的数组，任务是在 PHP 中打印一个数组的所有值 **arr** 。为了完成这个任务，我们在 PHP 中有以下方法:

**方法 1:使用** [**foreach 循环**](https://www.geeksforgeeks.org/php-foreach-loop/)**:**foreach 循环用于迭代数组元素。foreach 循环虽然迭代了一个元素数组，但执行过程得到了简化并结束了循环。

**语法:**

```php
foreach( $array as $element ) {
    // PHP Code to be executed
}

```

**示例:**

## PHP

```php
<?php
// PHP program to print all 
// the values of an array

// given array
$array = array("Geek1", "Geek2",
           "Geek3", "1", "2","3");  

// Loop through array
foreach($array as $item){
    echo $item . "\n";
}

?>
```

**输出**

```php
Geek1
Geek2
Geek3
1
2
3

```