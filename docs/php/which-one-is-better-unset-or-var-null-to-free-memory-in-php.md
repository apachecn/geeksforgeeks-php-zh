# PHP 中释放内存哪个更好(unset()还是$var = null)？

> 原文:[https://www . geeksforgeeks . org/哪个更好-取消设置-或-var-null 到-free-memory-in-php/](https://www.geeksforgeeks.org/which-one-is-better-unset-or-var-null-to-free-memory-in-php/)

在本文中，我们将讨论通过对任何变量使用空值来释放内存。

**unset():**unset()函数是 PHP 中的一个内置函数，用于取消指定变量的设置。 *unset()* 函数只是销毁或移除符号表中的变量。在变量上应用 *unset()* 后，它被标记为 PHP 垃圾收集。

**语法:**

```
unset($variable)
```

*   $未设置的变量

**示例:**以下示例演示了 **unset()** 功能。在下面的示例中，从变量堆栈中移除了$a 内存，在取消设置操作后$a 不再存在。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

    // Declare a variable and set
    // to some string
    $a = "hello geeks";
    echo "Before unset : $a";

    // Unset this variable
    unset($a);
    echo "<br>";

    // Display the variable
    echo "After unset : $a";
?>
```

**输出:**

```
Before unset : hello geeks
After unset :
```

**null:** null 用于清空变量。我们可以创建一个*空*变量，只需将其赋为空即可。不会释放内存，但会在该特定变量上重写或重新分配空数据。

**语法:**

```
$variable = null;
```

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

    // Declare a variable and
    // set to string
    $a = "Hello geeks";
    echo "Before null : $a";

    // Assign null to this variable
    $a = null;
    echo "<br>";

    // Display result
    echo "After null : $a";
?>
```

**输出:**

```
Before null : Hello geeks
After null :
```

**哪个更好？**

**取消设置()功能:**

*   **unset()** 不强制立即释放内存，用于释放变量使用。
*   PHP 垃圾收集器清理未设置的变量。
*   CPU 周期没有浪费
*   释放内存需要时间

**空变量:**

*   *空*变量立即释放内存。
*   浪费了 CPU 周期，并且需要更长的执行时间。
*   它迅速释放了内存。

**结论:如果一个变量需要的内存比较少，空**比较好。