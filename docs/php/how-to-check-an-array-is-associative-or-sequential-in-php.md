# 在 PHP 中如何检查数组是关联的还是顺序的？

> 原文:[https://www . geesforgeks . org/如何在 php 中检查数组是关联的还是顺序的/](https://www.geeksforgeeks.org/how-to-check-an-array-is-associative-or-sequential-in-php/)

在 PHP 中，不需要在变量之前写变量类型，因为它是松散类型的。它从存储在其中的用户定义值中获取数据类型。PHP 中的数组是一种数据结构，它允许在一个变量下存储多个相似数据类型的元素，从而节省了为每个数据创建不同变量的工作量。
PHP 中数组基本有三种类型:

*   **顺序(索引)数组**
*   **关联数组**
*   **多维数组**

**顺序数组:**那些以有序的顺序方式(从 0 开始，以 n-1 结束)具有数值索引的数组称为顺序数组或索引数组。在 PHP 中，默认情况下是数组索引数组。

```
<?php
// Example of sequential array

$arr = array("January", "February", "March");

// 1st element
echo $arr[0] . "\n";

// 2nd element
echo $arr[1] . "\n";

// 3rd element     
echo $arr[2] . "\n";
?>
```

**Output:**

```
January
February
March

```

**关联数组:**具有字符串类型键而不是索引的数组或存在于('键'，'值')对中的数组称为关联数组。

```
<?php
// Example of associative array

$arr1= array("Month1" => "January",
             "Month2" => "February",
             "Month3" => "March" 
        );

echo $arr1["Month1"] . "\n";
echo $arr1["Month2"] . "\n";
echo $arr1["Month3"] . "\n";
?>
```

**Output:**

```
January
February
March

```