# PHP 中==和===有什么区别？

> 原文:[https://www . geeksforgeeks . org/PHP 中的区别是什么/](https://www.geeksforgeeks.org/what-is-the-difference-between-and-in-php/)

在本文中，我们将讨论 PHP 中的' == '和' === '运算符之间的区别。两者都是比较运算符，用于比较两个或多个值。

**==运算符:**该运算符用于检查给定值是否相等。如果是，则返回*真*，否则返回*假*。

**语法:**

```
operand1 == operand2
```

**===运算符:**该运算符用于检查给定值及其数据类型是否相等。如果是，则返回*真*，否则返回*假*。

**语法:**

```
operand1 === operand2
```

**注意:** ===当操作数的数据类型不同时*，运算符将返回 *false* 。*

**示例 1:** 下面的代码演示了具有相同和不同数据类型操作数的==运算符。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

$a = 34;
$b = 34;

// Show message if two operands are
// equal with same data type operands
if($a == $b) {
    echo "Equal";
}
else{
    echo "Not Equal";
}

echo "\n";

// Show a message if two operands are equal
// with different data type operands
// First is of string type and the second
// is of integer type
if('34' == 34){
    echo "Equal";
}
else{
    echo "Not Equal";
}

?>
```

**输出:**

```
Equal
Equal
```

**示例 2:** 下面的代码演示了===运算符。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

$a = 34;
$b = 34;

// Return a message if two operands are
// equal with same data type operands
if($a === $b){
    echo "Equal";
}
else{
    echo "not Equal";
}

echo "\n";

// Return a message if two operands are equal
// with different data type operands
// First is of string type and the second
// is if integer type
if('34' === 34){
    echo "Equal";
}
else{
    echo "not Equal";
}

?>
```

**输出:**

```
Equal
not Equal
```

**区别==和===运算符:**

<figure class="table">

| **=** | **= =** |
| It is equal to the operator. | Is the same operator. |
| Used to check whether two operands are equal. | Used to check whether two operands and their data types are equal. |

</figure>