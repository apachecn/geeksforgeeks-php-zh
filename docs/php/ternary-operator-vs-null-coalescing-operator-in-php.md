# 三进制运算符 vs PHP 中的空合并运算符

> 原文:[https://www . geesforgeks . org/三元-运算符-vs-null-聚结-运算符-in-php/](https://www.geeksforgeeks.org/ternary-operator-vs-null-coalescing-operator-in-php/)

**三元运算符**

三进制运算符是条件运算符，它有助于在执行比较和条件运算时减少编码行数。这是使用 if else 和嵌套 if else 语句的另一种方法。执行的顺序是从左到右。这绝对是节省时间的最佳选择。当遇到带有条件的空值时，它确实会产生一个电子通知。

**语法:**

```
(Condition) ? (Statement1) : (Statement2);
```

在三元运算符中，如果条件语句为真，则语句 1 将执行，否则语句 2 将执行。

**条件运算的替代方法:**

```
if (Condition) {
    return Statement1;
} else {
    return Statement2;
}
```

**示例:**

```
<?php

// PHP program to check number is even
// or odd using ternary operator

// Assign number to variable
$num = 21;

// Check condition and display result
print ($num % 2 == 0) ? "Even Number" : "Odd Number";
?>
```

**Output:**

```
Odd Number

```

**空合并运算符**

空合并运算符用于检查给定变量是否为空，并从一对自定义值中返回非空值。空合并运算符主要用于避免对象函数返回空值，而不是返回默认的优化值。它用于避免异常和编译器错误，因为它在执行时不会产生电子通知。执行的顺序是从右到左。执行时，不为空的右侧操作数将是返回值，如果为空，则左侧操作数将是返回值。它有助于提高源代码的可读性。

**语法:**

```
(Condition) ? (Statement1) ? (Statement2);
```

**条件运算的替代方法:**

```
// The isset() function is used to take
// care that the condition is not NULL
if ( isset(Condition) ) {   
    return Statement1;
} else {
    return Statemnet2;
}
```

**示例:**

```
<?PHP

// PHP program to use Null 
// Coalescing Operator

// Assign value to variable
$num = 10;

// Use Null Coalescing Operator 
// and display result
print ($num) ?? "NULL";

?>
```

**Output:**

```
10

```

**三进制运算符和空合并运算符的区别:**

*   三元运算符是左关联的，其中空组合运算符是右关联的。
*   如果左操作数为空，三进制运算符抛出 e-note，而如果左操作数不存在，空合并运算符不会抛出 e-note。
*   三元运算符检查该值是否为真，但空组合运算符检查该值是否不为空。
*   如果要执行更多的迭代，则发现空合并运算符比三进制运算符更快。
*   相比之下，Null 合并运算符也提供了更好的可读性。