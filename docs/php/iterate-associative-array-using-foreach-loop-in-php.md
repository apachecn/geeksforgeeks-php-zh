# 在 PHP 中使用 foreach 循环迭代关联数组

> 原文:[https://www . geeksforgeeks . org/iterate-associative-array-using-foreach-loop-in-PHP/](https://www.geeksforgeeks.org/iterate-associative-array-using-foreach-loop-in-php/)

给定两个大小为 n 的数组 **arr1** 和 **arr2** ，任务是在 foreach 循环中迭代这两个数组。两个数组都可以使用 foreach 循环组合成一个数组。

**Array:**PHP 中的 Array 是一种数据结构，允许在单个变量下存储多个相似数据类型的元素，从而节省了为每个数据创建不同变量的工作量。数组有助于创建相似类型的元素列表，可以通过使用它们的索引或键来访问这些元素。

**例:**

```php
Input : $sides = array('Up', 'Down', 'Left', 'Right')
        $directions = array('North', 'South', 'West', 'East')

Output :
Up => North
Down => South
Left => West
Right => East

```

**示例 1:** 本示例使用 foreach 循环显示关联数组的元素。

```php
<?php

// Declare an associative array
$aso_arr = array(
    "Up"=>"North", 
    "Down"=>"South", 
    "Left"=>"West", 
    "Right"=>"East"
);

// Use foreach loop to traverse each
// elements of array and display its
// key and value 
foreach($aso_arr as $side=>$direc) {
    echo $side . " => " . $direc . "\n"; 
}

?>
```

**输出:**

```php
Up => North
Down => South
Left => West
Right => East

```