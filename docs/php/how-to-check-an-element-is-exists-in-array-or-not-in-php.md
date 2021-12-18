# 在 PHP 中如何检查一个元素是否存在于数组中？

> 原文:[https://www . geesforgeks . org/如何检查一个元素是否存在于数组中 php/](https://www.geeksforgeeks.org/how-to-check-an-element-is-exists-in-array-or-not-in-php/)

数组可能包含属于不同数据类型、整数、字符或逻辑类型的元素。然后可以使用各种内置方法在阵列中检查这些值:

**方法 1(使用**[**in _ array()**](https://www.geeksforgeeks.org/php-in_array-function/)**方法):**可以使用 [array()](https://www.geeksforgeeks.org/php-arrays/) 方法声明一个数组。PHP 中的 **in_array()** 方法用于检查数组中是否存在元素。该方法返回*真*或*假*，这取决于该元素是否存在于数组中。

```
in_array(element , array)
```

**论据:**

*   **元素:**数组中要检查的元素
*   **数组:**要寻找元素的数组

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Declaring an array object 
$arr = array("Hello", "GEEKs" , "User" , "PHP");
print("Original Array </br>");
print (json_encode($arr) . " </br>");

// Declaring element
$ele = "GEEKs";

// Check if element exists
if(in_array($ele, $arr)){
    print($ele . " - Element found.");
}else{
    print($ele . "Element not found.");
}
?>
```

**输出:**

```
Original Array:
["Hello","GEEKs","User","PHP"]
GEEKs - Element found.
```

**方法 2(使用** [**进行**](https://www.geeksforgeeks.org/php-loops/) **循环):**在整个数组中进行循环迭代。声明一个布尔标志来检查元素的存在。它被初始化为布尔值*假*。如果值为*假*，并且在数组中找到该元素，则标志值变为*真*值。标志值没有进一步修改。

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Declaring an array object 
$arr = array(1, 3, 5, 6);
print("Original Array </br>");
print (json_encode($arr)." </br>");

// Declaring element
$ele = 5;

// Declare a flag 
$flag = FALSE;

// Check if element exists
foreach($arr as $val){
    if($flag == FALSE){
        if($val == $ele){
            $flag = TRUE;
        }
    }
}
if($flag ==TRUE){
    print($ele . " - Element found.");
}
else{
    print($ele . " - Element not found.");
}
?>
```

**输出:**

```
Original Array
[1, 3, 5, 6]
5 - Element found.
```