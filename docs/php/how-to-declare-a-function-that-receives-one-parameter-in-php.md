# 如何在 PHP 中声明接收一个参数的函数？

> 原文:[https://www . geeksforgeeks . org/如何声明在 php 中接收一个参数的函数/](https://www.geeksforgeeks.org/how-to-declare-a-function-that-receives-one-parameter-in-php/)

在本文中，我们将知道如何在 PHP 中声明接收单个参数的函数。函数调用是任何编程语言的一个重要方面。可以在脚本中调用函数(方法)来简化操作的性能，并消除在多个点编写相同代码片段的冗余。函数可以用用户定义的名称和用户定义的签名来声明。

本文将给出调用参数化函数的想法，该函数只接受一个名为“hello”的参数作为输入。然后调用该函数，绕过任意布尔值，并将其分配给正在调用的函数参数值。调用函数也称为父函数。下图说明了所使用的方法:

函数中使用的以下术语将有助于理解函数的工作原理。

**参数传递:**所需参数可以作为参数在父函数中传递。该值可由接收功能接收，该功能可用于执行主要操作&显示传递的参数。从父函数传递的值被赋给接收函数&中声明的变量，它可以在代码的其他部分使用。

**参数接收:**参数可以在接收功能中操作和显示，也可以从那里作为值返回最终输出。这主要是在调用/父方法需要进一步分析输出的情况下完成的。然后以声明变量的形式接收该值。例如，在上图中， *resp* 变量被赋予返回值 *x* 。

基于接收到的值，该函数可以显示输出，其形式为字符串。如果接收到 true 作为参数值，该方法将打印“Hello”，否则将返回 false。返回值是方法的输出。但是，调用的函数，即子方法，有时可能会在其自己的代码段中显示输出，如下所示。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

function param_hello($hello=false){
    if($hello){
      echo("Hello </br>");
    }
    else{
      echo("No hello </br>");
    }

}

// Calling function first time
param_hello(true);
param_hello(false);

?>
```

**输出:**

```php
Hello
No hello
```

该函数也可能返回一个输出对象，而不是在那里打印它。然后可以从调用语句中捕获响应，并显示在脚本中。

**示例:**本示例描述了根据应用的条件，在脚本中显示函数返回值。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
function param_hello($hello=false){
    if($hello){
      return "Hello </br>";
    }
    else{
      return "No hello </br>";
    }
}

$flag = true;

// Calling function first time
$res = param_hello($flag);
echo($res);
?>
```

**输出:**

```php
Hello
```