# PHP 中 for vs foreach 的性能

> 原文:[https://www . geesforgeks . org/performance-of-for-vs-foreach-in-PHP/](https://www.geeksforgeeks.org/performance-of-for-vs-foreach-in-php/)

**for 循环:**for 循环是一个迭代循环，它重复一组特定的代码，直到达到指定的条件。它被系统地用于执行一组指定次数的代码，这里的次数表示迭代器变量。

**语法:**

```php
for( initialization; condition; increment/decrement ) {
    // Set of Code to be iterated and executed
}
```

for 循环的每个参数都有独特的功能，为了更好地理解，下面对这些功能进行了说明:

*   **初始化:**用于初始化迭代器变量，并在循环条件开始时一次性执行，而不运行条件语句，循环条件是循环中代码集的第一次执行。
*   **条件:**在每次迭代的开始，执行条件语句，如果条件返回真值，循环继续，执行代码集中的嵌套语句。如果条件的计算结果为 false，循环的执行将在代码的该点中断。
*   **增量:**它用一个新的增量值来增加循环计数器，该值将为条件语句计算。它在每次迭代结束时被强制执行，没有任何中断。

**示例:**本示例使用以$j = 1 开头的 for 循环。循环将持续到$j 小于或等于 5。每次循环运行时，变量$j 将增加 1。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Loop starts from here
for($j = 1; $j <= 5; $j++) {
    echo $j . " GeeksforGeeks \n";
}

?>
```

**Output:** 

```php
1 GeeksforGeeks 
2 GeeksforGeeks 
3 GeeksforGeeks 
4 GeeksforGeeks 
5 GeeksforGeeks
```