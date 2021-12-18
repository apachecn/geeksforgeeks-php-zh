# 如何在 PHP 中使用 array_pop()和 array_push()方法？

> 原文:[https://www . geesforgeks . org/如何使用 array _ pop-and-array _ push-methods-in-PHP/](https://www.geeksforgeeks.org/how-to-use-array_pop-and-array_push-methods-in-php/)

PHP 中的 [array_push()](https://www.geeksforgeeks.org/php-array_push-function/) 和 [array_pop()](https://www.geeksforgeeks.org/php-array_pop-function/) 方法用于执行对象的插入和删除。下面的文章说明了这些方法的用法:

**使用** [**array_push()方法**](https://www.geeksforgeeks.org/php-array_push-function/)**:**array _ push()方法用于推送数组集合对象中的多个元素。在每个 array_push()方法之后，数组对象的大小会增加方法调用中指定的元素数量。

```
array_push($array, $elements)
```

**参数:**

*   **$ array–**元素被推入的数组。
*   **$ elements–**在数组中推送的元素。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Declaring an array
$arr = array();

// Adding the first element
array_push($arr, 1);

print("Array after first addition </br>");
print_r($arr);
print("</br>");

// Adding second element
array_push($arr, 2);
print("Array after second addition </br>");
print_r($arr);

?>
```

**Output**

```
Array after first addition </br>Array
(
    [0] => 1
)
</br>Array after second addition </br>Array
(
    [0] => 1
    [1] => 2
)
```

array_push()方法用于同时推送数组中的多个元素。元素按照它们在方法调用中指定的顺序插入。以下代码片段指示了该过程:

```
array_push($array, $ele1, $ele2, ...)
```

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Declaring an array
$arr = array();

// Adding the first element
array_push($arr, 1, 2, 3, 4, 5);

print_r("Array after multiple insertions </br>");

print_r($arr);
?>
```

**Output**

```
Array after multiple insertions </br>Array
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
)
```

**使用 array_pop()方法:**array _ pop()方法用于从数组中弹出元素。每次调用此方法时，都会从末尾逐个移除元素。

```
array_pop($array)
```

**参数:**函数只取一个参数$array，即输入数组，从中弹出最后一个元素，将大小减少一。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Declaring an array
$arr = array();

// Adding the first element
array_push($arr, 1, 2, 3, 4, 5);

print_r("Array after multiple insertions </br>");
print_r($arr);
array_pop($arr);

// Single array pop
print_r("Array after a single pop </br>");
print_r($arr);

?>
```

**Output**

```
Array after multiple insertions </br>Array
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
)
Array after a single pop </br>Array
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
)
```