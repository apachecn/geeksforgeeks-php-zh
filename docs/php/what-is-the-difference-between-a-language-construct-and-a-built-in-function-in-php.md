# PHP 中的语言构造和“内置”函数有什么区别？

> 原文:[https://www . geesforgeks . org/语言构造和 php 内置函数的区别是什么/](https://www.geeksforgeeks.org/what-is-the-difference-between-a-language-construct-and-a-built-in-function-in-php/)

在编程中，语言构造和内置函数经常被误解，因为两者或多或少都有相似的行为。但是它们在 PHP 解释器的解释方式上有所不同。每种编程语言都由各自语言解析器能够识别的标记和结构组成。因此，每当一个文件被解析时，解析器理解它们的用法，并且知道如何处理它们，而不需要进一步检查它们。这些标记和结构被称为**语言结构**。它们基本上是作为编程语言一部分的关键字。换句话说，它们构成了语言的句法。
以下是一些语言结构的例子:

```
echo()
include()
require()
print()
isset()
die()

```

语言构造不能通过任何插件或库添加到 PHP 框架中。它们可能会也可能不会返回任何值，尽管大多数都不会。此外，其中一些不需要使用括号。

以下示例说明了 PHP 中语言构造的使用:
**示例 1:**

```
<?php

 print('Monday ');
 print 'Tuesday ';
 $str = 'Wednesday';
 echo $str;

?>
```

**Output:**

```
Monday Tuesday Wednesday

```

**例 2:**

```
<?php
/* PHP program to use unset
function */

$arr = array(
    "1" => "Amit",
    "2" => "Rajeev",
    "3" => "Mohit",
    "4" => "Manoj"
);

// Use unset function to
// unset element
unset($arr["2"]);

// Display array element
print_r($arr);

?>
```

**Output:**

```
Array
(
    [1] => Amit
    [3] => Mohit
    [4] => Manoj
)

```

另一方面，**内置函数**是以这样一种方式记录下来的代码块，它们可以在执行特定任务时一次又一次地被重用。它们已经存在于 PHP 安装包中。正是由于这些内置函数，PHP 才是一种高效的脚本语言。
PHP 中常用的一些内置函数有:

```
json_encode()
mail()
explode()
rand()
curl_init()

```

内置函数比它们的语言结构相对慢。他们有更好的代码组织。它们通常接受输入参数并总是返回值。内置函数通常由日期、数字和字符串函数组成。

以下示例说明了内置函数在 PHP 中的使用:
**示例 1:**

```
<?php
/* Date functions in PHP */

 echo" Date and time is - ";
 print date("j F Y, g.i.a", time());

?>
```

**Output:**

```
Date and time is - 26 February 2019, 12.22.pm

```

**例 2:**

```
<?php
/* String functions in PHP */

 $MyStr = "GeeksForGeeks";
 echo substr("GeeksForGeeks", 5, 3)."\n";
 echo trim("   GeeksForGeeks    ")."\n"; 
 echo str_replace("Geeks", "Code", "GeeksForGeeks");

?>
```

**Output:**

```
For
GeeksForGeeks
CodeForCode

```