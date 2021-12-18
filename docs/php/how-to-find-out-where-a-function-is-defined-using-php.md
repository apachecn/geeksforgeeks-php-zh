# 如何用 PHP 找出一个函数的定义位置？

> 原文:[https://www . geeksforgeeks . org/如何使用 php/](https://www.geeksforgeeks.org/how-to-find-out-where-a-function-is-defined-using-php/) 找到函数的定义位置

当我们做项目时，它包括多个模块，每个模块分成多个文件，每个文件包含多行代码。所以当我们在文件的某个地方声明一个函数时，忘记了这个函数在做什么，或者想改变这个函数的代码，但是找不到这个函数在哪里！因此本文将帮助您找到函数的位置。
为了获得函数在 PHP 中的位置，我们可以使用内置类 **ReflectionFunction()** 。当我们需要详细信息的函数的名称被传递给类构造函数时，它会得到关于该函数的一些详细信息。

*   **getFileName:** 返回函数的文件位置。
*   **getNumberOfParameters:** 返回传递给函数的参数个数。
*   **getStartLine:** 它返回函数的起始行。

**语法:**

```
$details = new ReflectionFunction('function_name');
```

然后使用上面的函数访问您需要的任何内容。将下面的代码粘贴到主代码中，您将获得该函数的详细信息。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
$details = new ReflectionFunction('printing');
print $details->getFileName() . ':' . $details->getStartLine();
?>
```

**运行代码的步骤:**

*   创建一个名为*文件名. php* 的文件
*   将上面给出的代码复制到文件中。
*   将文件保存到本地主机服务器文件夹中。在 WampServer 的情况下，在 c 盘的“wamp64”文件夹中寻找“www”文件夹，并将文件保存在那里。
*   运行你的 wamp 服务器。
*   打开任意浏览器，输入 localhost/fun.php，得到如下输出。

**输出:**

```
C:\wamp64\www\file_name.php : 2 
```

以下示例说明了 PHP 中的 ReflectionFunction:
**示例 1:** 假设在给定的代码中，我们想要找到函数“打印”的位置。在输出中，可以看到函数打印的文件名和位置。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
function printing()
{
    echo 'Welcome to GeeksforGeeks';
}

$details = new ReflectionFunction('printing');
echo 'File location : '.$details->getFileName().
', Starting line : ' . $details->getStartLine().
', Parameters passed : '.$details->getNumberOfParameters();
?>
```

**输出:**

```
File location : /home/7de5f19b219d214c719df5f3839a7f61.php, 
Starting line : 2, Parameters passed : 0
```

**示例 2:** 假设在给定的代码中，我们想要找到函数“极客”的位置。在输出中，可以看到函数极客传递的文件名、位置、开始行和参数。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

function printing() {
    echo 'Welcome to GeeksforGeeks';
}

function geeks() {
    echo 'This is the article How to find out where
         a function is defined using PHP?';
}

$details = new ReflectionFunction('geeks');

print 'File location :'.$details->getFileName().
' Starting line :' . $details->getStartLine().
' No. of parameters passed :'.$details->getNumberOfParameters();

?>
```

**输出:**

```
File location :/home/dd96d70bdf5ff03fea0ea24110bae9ff.php 
Starting line :7 No. of parameters passed :0
```