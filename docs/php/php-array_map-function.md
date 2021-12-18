# PHP | array_map()函数

> 原文:[https://www.geeksforgeeks.org/php-array_map-function/](https://www.geeksforgeeks.org/php-array_map-function/)

array_map()是 PHP 中的一个内置函数，它有助于根据用户定义的条件以简单的方式修改一个或多个数组中的所有元素。基本上，它将数组的每个元素发送给用户定义的函数，并返回一个带有该函数修改后的新值的数组。

**语法**:

```
array_map(functionName,arr1,arr2...)

```

**所用参数** :
该功能取 2 个必选参数*功能名*和 *arr1* ，其余可选。

*   **函数名**(必选):该参数定义用户自定义函数的名称，根据该名称修改数组中的值。
*   **arr1** (必选):该参数指定要修改的数组。
*   **arr2** (必选):该参数指定要修改的数组。

functionName 参数是必需的，我们可以将任意数量的数组传递给这个名为 arr1，arr2 的函数..阿伦等等。

**返回类型:**此函数在对每个 arr1 应用 user_function()后，返回一个包含 arr 1 所有元素的数组。

下面的程序说明了 PHP 中 array_map()函数的工作原理:

```
<?php

function fun1($v)
{
  return ($v + 7);     // add 7 
}

function fun2($v1,$v2)
{
    if ($v1 == $v2) return 1;     
    else return 0;  
}

$arr1 = array(1, 2, 3, 4, 5);
$arr2 = array(1, 3, 3, 4, 8);

print_r(array_map("fun1", $arr1));

print_r(array_map("fun2", $arr1, $arr2));

?>
```

输出:

```
Array
(
    [0] => 8
    [1] => 9
    [2] => 10
    [3] => 11
    [4] => 12
)
Array
(
    [0] => 1
    [1] => 0
    [2] => 1
    [3] => 1
    [4] => 0
)

```

**使用 array_map()** 创建数组的数组:我们也可以使用 PHP 中的 array_map()函数来创建数组的数组。为此，我们必须传递 *null* 作为参数来代替 *functionName* 参数和数组列表，以创建数组数组。

下面的程序演示了如何创建数组数组:

```
<?php
$a = array(1, 2, 3);
$b = array("one", "two", "three");

$result = array_map(null, $a, $b);

print_r($result);
?>
```

输出:

```
Array
(
    [0] => Array
        (
            [0] => 1
            [1] => one
        )

    [1] => Array
        (
            [0] => 2
            [1] => two
        )

    [2] => Array
        (
            [0] => 3
            [1] => three
        )

)

```