# PHP 回显和打印

> Original: [https://www.geeksforgeeks.org/php-echo-print/](https://www.geeksforgeeks.org/php-echo-print/)

在本文中，我们将了解什么是 PHP 中的 ECHO 和 PRINT 语句，并通过示例了解它们的基本实现。 回声用于显示传递给它的参数的输出。 它显示用逗号分隔的一个或多个字符串的输出。 Print 一次接受一个参数，不能在 PHP 中用作变量函数。 打印仅输出字符串。

**注意：**两者都是 PHP 程序中的[语言构造](https://www.geeksforgeeks.org/what-is-the-difference-between-a-language-construct-and-a-built-in-function-in-php/)，它们与用于在浏览器屏幕上输出数据的 PHP 程序或多或少相同。 *PRINT*语句是*ECHO*的替代语句。

**PHP ECHO 语句：**它是一种语言构造，其行为从来不像函数，因此不需要括号。 但是，如果开发人员愿意，可以使用括号。 *ECHO*语句的末尾由分号(‘；’)标识。 *它输出一个或多个字符串。 我们可以使用‘*ECHO*’输出字符串、数字、变量、值和表达式结果。 以下是 PHP 中 ECHO 语句的一些用法：

**显示字符串**：我们可以简单地使用关键字*ECHO*，后跟要在引号中显示的字符串。 下面的示例显示如何使用 PHP 显示字符串。

## PHP

```php
<?php
    echo "Hello,This is a display string example!";
?>
```

发帖主题：Re：Колибри0.7.0

```php
Hello,This is a display string example!
```

**将字符串显示为多个参数**：我们可以向*ECHO*语句传递多个字符串参数，而不是单个字符串参数，并用逗号(‘，’)操作符分隔它们。 例如，如果我们有两个字符串，即“Hello”和“World”，那么我们可以将它们作为(“Hello”，“World”)传递。

## PHP

```php
<?php
    echo "Multiple ","argument ","string!";
?>
```

**输出：**

```php
Multiple argument string!
```

**显示变量**：使用*ECHO*语句显示变量也与显示普通字符串一样简单。 下面的示例展示了在 PHP*ECHO*语句的帮助下显示变量的不同方式。

## PHP

```php
<?php
  // Defining the variables
  $text = "Hello, World!";
  $num1 = 10;
  $num2 = 20;

  // Echoing the variables
  echo $text."\n";
  echo $num1."+".$num2."=";
  echo $num1 + $num2;
?>
```

**输出：**

```php
Hello, World!
10+20=30
```

上面代码中的**(.)**运算符可用于连接 PHP 中的两个字符串，“\n”用于换行，也称为换行符。 我们将在后续文章中了解这些内容。

**PHP print 语句：**PHP*print*语句类似于*ECHO*语句，可以多次替代*ECHO*使用。 它也是一种语言构造，因此我们不能使用括号，即*print*或*print()*。

*PRINT*和*ECHO*语句之间的主要区别在于，*ECHO*的行为不像函数，而*Print*的行为像函数。 *print*语句一次只能有一个参数，因此可以打印单个字符串。 此外，*PRINT*语句总是返回值 1。与*ECHO*类似，*PRINT*语句也可用于打印字符串和变量。 以下是在 PHP 中使用*print*语句的一些示例：

**显示文本字符串**：我们可以使用*print*语句显示字符串，方法与使用*cho*语句相同。 唯一的区别是，我们不能用一条打印语句显示由逗号(，)分隔的多个字符串。 下面的示例显示如何在 PHP*PRINT*语句的帮助下显示字符串。

## PHP

```php
<?php
    print "Hello, world!";
?>
```

**输出：**

```php
Hello, world!
```

**显示变量**：使用*PRINT*语句显示变量也与使用*ECHO*语句相同。 下面的示例显示了如何在 PHP 打印语句的帮助下显示变量。

## PHP

```php
<?php

  // Defining the variables
  $text = "Hello, World!";
  $num1 = 10;
  $num2 = 20;

  // Echoing the variables
  print $text."\n";
  print $num1."+".$num2."=";
  print $num1 + $num2;
?>
```

**输出：**

```php
Hello, World!
10+20=30
```

**PHP 中 ECHO 和 PRINT 语句的差异：**

<figure class="table">

| _。 _ | 

#### ECHO statement

 | The

#### PRINT statement

 |
| --- | --- | --- |
| 

#### 1\.

 | ECHO accepts a comma-separated list of parameters (multiple parameters can be passed). | Print accepts only one parameter at a time. |
| 

#### 2\.

 | it does not return a value or void. | it returns a value of 1\. |
| 

#### 3\.

 | it displays the output of one or more strings separated by commas. | print only the string. |
| 

#### 4\.

 | it is much faster than PRINT statements. | it is slower than the ECHO statement. |

</figure>

**引用**：

*   [http：//php.net/manual/en/function.echo.php](http://php.net/manual/en/function.echo.php)
*   [http：//php.net/manual/en/function.print.php](http://php.net/manual/en/function.print.php)

本文由**Barun Gupta**贡献。 如果你喜欢 GeeksforGeek 并想投稿，你也可以使用[write.geeksforgeeks.org](http://www.write.geeksforgeeks.org)写一篇文章，或者把你的文章邮寄到 Review-team@geeksforgeeks.org。 看看你的文章出现在 GeeksforGeek 主页上，并帮助其他 Geek。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的主题的信息，请写下评论。