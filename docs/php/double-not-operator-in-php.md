# 双非(！！)PHP 中的运算符

> 原文:[https://www.geeksforgeeks.org/double-not-operator-in-php/](https://www.geeksforgeeks.org/double-not-operator-in-php/)

“非非”运算符或双非(！！)运算符只是返回变量或表达式的真值。用很简单的话来解释，第一个不是运算符(！)否定表达式。第二个不是运算符(！)再次否定表达式，得到之前存在的真值。

(！！)运算符作为布尔函数返回。如果用！！对一个表达式来说，真值是真的，假值是假的。布尔值没有变化。通过使用这个 double not(！！)运算符它可以增加代码的可读性，还可以确保真值和假值都是严格的布尔数据类型。

**例 1:**

```
<?php

// Declare a variable 
// and initialize it
$a = 1;

// Use double not operator
$a = !!$a;

// Display the value 
// of variable a.
echo $a;
?>
```

**逻辑非(！)运算符和 Double NOT(！！)PHP 中的运算符:**Not 运算符是数学上对相关数据的布尔值的补充或否定。例如，一个布尔值$a =真，那么非运算符强加给它！一美元是假的。这是关于逻辑非或否定运算符。哪里作为双非(！！)运算符仅返回布尔转换或真值。那是！！$a 始终为真。
这里还有一个基于双非运算符的例子。

**例 2:**

```
<?php

// PHP program to illustrate
// Double NOT operator

// Declare a variable and 
// initialize it
$t = 10;

// Check condition
if ($t !== 10)
    echo "This is NOT operator!";
elseif (!!$t)
    echo "This is Double NOT operator!";
else
    echo "Finish!";
?>
```

上面的代码严格保存了布尔数据类型，并返回变量的真值。