# PHP 中 for 和 Foreach 循环有什么区别？

> 原文:[https://www . geeksforgeeks . org/for-for-foreach-in-loop-PHP 的区别是什么/](https://www.geeksforgeeks.org/what-is-the-difference-between-for-and-foreach-loop-in-php/)

在 PHP 中，循环可以用来迭代集合对象。[](https://www.geeksforgeeks.org/php-loops/)**和 [*foreach*](https://www.geeksforgeeks.org/php-foreach-loop/) 循环可用于迭代元素。**

**[***为*** **循环:**](https://www.geeksforgeeks.org/php-loops/)***为*循环在给定条件结束时工作。它用于实现变量，并且以单一方式工作。在关联数组的情况下，循环的*不起作用。用于*回路的*基本上由三个部分组成。*****

*   ****变量用一个值初始化。****
*   ****变量受制于与之比较的条件。****
*   ****递增/递减循环计数器。****

```
****for(expr1; expr2; expr3) {
    // Perform action
}****
```

******例 1:******

## ****服务器端编程语言（Professional Hypertext Preprocessor 的缩写）****

```
****<?php

// Declaring an array
$arr = array(1, 2, 3, 4, 5);

// Looping over array
for($i = 0; $i < 5; $i++) {

// Accessing individual elements
    echo($arr[$i] . "  ");
}

?>****
```

******输出:******

```
****1  2  3  4  5**** 
```

****[**foreach 循环**](https://www.geeksforgeeks.org/php-foreach-loop/)**:***foreach*循环在数组计数结束时工作。这个循环可以处理变量以及[关联数组](https://www.geeksforgeeks.org/associative-arrays-in-php/)。因此，这个循环可以用多种方式实现。 *foreach* 循环比 *for* 循环要好得多，性能也更好。****

```
****foreach ($array as $value) {
    // Perform action
}****
```

******例 2:******

## ****服务器端编程语言（Professional Hypertext Preprocessor 的缩写）****

```
****<?php

// Declaring an array
$arr = array(1, 2, 3, 4, 5);

// Looping over array
foreach($arr as $val){

    // Accessing individual elements
    echo($val . "  ");
}

?>****
```

******输出:******

```
****1  2  3  4  5**** 
```

****这个循环也可以在键值对的情况下实现，即关联数组。按键及其对应的映射值可以很容易地显示在屏幕上。下面的代码片段说明了循环在[关联数组](https://www.geeksforgeeks.org/associative-arrays-in-php/)上的用法。****

```
****foreach ($array as $key => $value) {
    // Perform action
}****
```

******例 3:******

## ****服务器端编程语言（Professional Hypertext Preprocessor 的缩写）****

```
****<?php

// Declaring an array
$arr = array();
$arr["Java"] = "Spring Boot";
$arr["PHP"] = "CodeIgniter";
$arr["Python"] = "Django";

// Looping over array
foreach($arr as $key => $val) {

    // Accessing individual elements
    echo($key . " : " . $val . "<br>");
}

?>****
```

******输出:******

```
****Java : Spring Boot
PHP : CodeIgniter
Python : Django****
```

<figure class="table">

| **为循环** | **前循环** |
| 迭代清晰可见。 | 迭代是隐藏的。 |
| 表现不错。 | 性能更好。 |
| 停止条件很容易指定。 | 必须明确指定停止条件。 |
| 在处理集合时，它需要使用 [**【计数】(**](https://www.geeksforgeeks.org/php-count-function/) 功能。 | 没有[**的用法，它可以简单地工作()**](https://www.geeksforgeeks.org/php-count-function/) 方法。 |

</figure>