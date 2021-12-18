# 在 PHP 中如何获取数组逆序的元素？

> 原文:[https://www . geeksforgeeks . org/如何以 php 数组逆序获取元素/](https://www.geeksforgeeks.org/how-to-get-elements-in-reverse-order-of-an-array-in-php/)

数组是存储在一起的元素的集合。数组中的每个元素都属于类似的数据类型。数组中的元素通过它们的索引值来识别。这些元素可以进行各种操作，包括反转。有多种方法可以反转数组的元素:

**方法 1:** 使用**进行循环，**可以启动循环减量，以便以相反的顺序访问元素。索引从数组的长度–1 开始，直到到达数组的开头。在每次迭代期间，都会调用内置的 array_push 方法，该方法用于将元素推送到为存储反向内容而维护的新声明的数组中。

**语法:**

```
array_push($array, $element)
```

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
    // Declaring an array
    $arr = array(1, 2, 3, 4, 5);
    echo("Original Array : ");
    print_r($arr);

    // Declaring an array to store reverse
    $arr_rev = array();
    for($i = sizeof($arr) - 1; $i >= 0; $i--) {
        array_push($arr_rev,$arr[$i]);
    }

    echo("Modified Array : ");
    print_r($arr_rev);
?>
```

**Output**

```
Original Array : Array
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
)
Modified Array : Array
(
    [0] => 5
    [1] => 4
    [2] => 3
    [3] => 2
    [4] => 1
)
```

**方法二:**使用 [**array_reverse()方法**](https://www.geeksforgeeks.org/php-array_reverse-function/) **、t** he array_reverse()函数可用于反转指定数组的内容。输出也以数组的形式返回。

**语法:**

```
array_reverse($array)
```

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
    // Declaring an array
    $arr = array(1, 2, 3, 4, 5);
    echo("Original Array : ");
    print_r($arr);

    // Reversing array
    $arr_rev = array_reverse($arr);
    echo("Modified Array : ");
    print_r($arr_rev);
?>
```

**Output**

```
Original Array : Array
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
)
Modified Array : Array
(
    [0] => 5
    [1] => 4
    [2] => 3
    [3] => 2
    [4] => 1
)
```