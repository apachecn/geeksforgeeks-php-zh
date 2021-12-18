# PHP |基本语法

> 原文:[https://www.geeksforgeeks.org/php-basic-syntax/](https://www.geeksforgeeks.org/php-basic-syntax/)

定义 PHP 计算机语言的结构叫做 **PHP 语法**。

PHP 脚本在服务器上执行，HTML 结果被发送到浏览器。它通常可以有 HTML 和 PHP 标签。PHP 或超文本预处理器是一种广泛使用的开源通用脚本语言，可以嵌入 HTML。PHP 文件用“.”保存。php "扩展。PHP 脚本可以和普通的 HTML 一起用 PHP 标签写在文档的任何地方。

**逃到 PHP:**

在 *<里面写 PHP 代码？php …？>* 叫做**逃到 PHP** 。

从 PHP 代码中分离普通 HTML 的机制被称为转义成 PHP 的机制。有多种方法可以做到这一点。默认情况下已经设置了很少的方法，但是为了使用很少的其他方法，比如短开或 ASP 风格的标签，我们需要更改 *php.ini* 文件的配置。这些标签也用于在 HTML 中嵌入 PHP。有 4 个这样的标签可用于此目的。

**规范 PHP 标签**:脚本以 **<开头？php** 以**结尾？>** 。这些标签也被称为“规范 PHP 标签”。PHP 解析器会忽略一对开始和结束标记之外的所有内容。开始和结束标记称为分隔符。每个 PHP 命令都以分号(**)结束；**)。我们来看看 PHP 中的 *hello world* 程序。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
# Here echo command is used to print
echo "Hello, world!";
?>
```

**输出:**

```php
Hello, world!
```

**SGML 或短 HTML 标签**:这是初始化一个 PHP 代码的最短选项。剧本以 **<开头？**以**结尾？>** 。这只能通过将 *php.ini* 文件中的 *short_open_tag* 设置设置为“开”来实现。

**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?
# Here echo command will only work if
# setting is done as said before
echo "Hello, world!";
?>
```

**输出:**

```php
Hello, world!
```

**HTML 脚本标签**:这些都是使用脚本标签实现的。PHP 7.0.0 中删除了该语法。所以不再使用了。

**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<script language="php">
echo "hello world!";
</script>
```

**输出:**

```php
hello world!
```

**ASP 样式标签**:要使用这个，我们需要设置 *php.ini* 文件的配置。活动服务器页面使用它们来描述代码块。这些标签以 **< %** 开始，以 **% >** 结束。

**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<%
# Can only be written if setting is turned on
# to allow %
echo "hello world";
%>
```

**输出:**

```php
hello world
```

**常数:**

常数可以使用 *const* 关键字或 [define()](https://www.geeksforgeeks.org/php-defined-function/) 函数来定义。

常量和变量之间有一些区别。

*   常量前面不像变量前面有$号。
*   可以从任何地方访问常量，而无需考虑变量范围规则。

**PHP 中的注释:**

如果代码在一段时间后被重新访问，注释有助于提醒开发人员。

注释是被忽略的东西，不被 PHP 引擎或语言作为程序的一部分读取或执行，它的编写是为了使代码更可读和更容易理解。这些用于帮助其他用户和开发人员描述代码以及它试图做什么。它也可以用于记录一组代码或程序的一部分。您一定在上面的示例程序中注意到了这一点。
PHP 支持两种类型的注释:

*   **单行注释**:顾名思义，这些是可以添加到代码中的单行或简短的相关解释。要补充这一点，我们需要以( **//** )或( **#** )开头。

**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
// This is a single line comment
// These cannot be extended to more lines

echo "hello world!!!";

# This is also a single line comment
?>
```

**输出:**

```php
hello world!!!
```

*   **多行或多行注释**:用于容纳单个标签的多行，可以根据用户需要扩展到多行。要添加此内容，我们需要以(**/*……*/**)
    开始和结束该行

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
/* This is a multi line comment
    In PHP variables are written
    by adding a $ sign at the beginning.*/

$geek = "hello world!";
echo $geek;
?>
```

**输出:**

```php
hello world!
```

**PHP 中的区分大小写:**

*   **PHP 对空白不敏感。**这包括屏幕上不可见的所有类型的空格，包括制表符、空格和回车。即使一个空格也等于任意数量的空格或回车。这意味着 PHP 将忽略单行中的所有空格或制表符，或者多行中的回车。除非遇到分号，否则 PHP 会将多行视为单个命令。

**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
// PHP code illustrate the whitespace insensitivity
$var1         =     15;
$var2 =
30;
$sum = $var1
+
$var2;

// "\n" for new line
echo $sum, "\n";

$sum1 = $var1 + $var2;
echo $sum1;
?>
```

**输出:**

```php
45
45
```

两者显示相同的结果，没有任何错误。

*   **PHP 区分大小写**。PHP 中的所有关键字、函数和类名(while、if、echo、else 等)除变量外不区分大小写。只有不同情况的变量才会被区别对待。让我们看看这个例子:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
// Here we can see that all echo
// statements are executed in the same manner

$variable = 25;
echo $variable;
ECHO $variable;
EcHo $variable;

// but this line will show RUNTIME ERROR as
// "Undefined Variable"
echo $VARIABLE
?>
```

**输出:**

```php
25
25
25
```

**PHP 中的块:**

在 PHP 中，通过使用花括号( **{}** )可以同时执行多个语句(在单个条件或循环下)。这形成了同时执行的语句块。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
$var = 50;
if ($var>0){
    echo ("Positive as \n");
    echo ("greater than 0");
}
?>
```

**或****【tput:**

```php
Positive as
greater than 0
```

本文由**钦莫伊·蕾恩卡**供稿。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。