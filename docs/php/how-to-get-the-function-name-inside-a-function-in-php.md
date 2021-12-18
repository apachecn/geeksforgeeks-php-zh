# 如何在 PHP 中获取函数内部的函数名？

> 原文:[https://www . geeksforgeeks . org/如何在 php 函数中获取函数名/](https://www.geeksforgeeks.org/how-to-get-the-function-name-inside-a-function-in-php/)

要获取 PHP 函数内部的函数名，我们需要使用*(_ _ FUNCTION _ _)。*

***魔法常数:**魔法常数是 PHP 中预先定义的常数，是在使用的基础上使用的。这些常量以双下划线(__)开头和结尾。这些常数由各种扩展创建。*

***语法:***

```php
*$string = __FUNCTION__*
```

***说明:**这个常量是用来返回函数名的，或者是匿名函数的*{闭包}* 。*

***程序 1:** PHP 程序打印函数里面的函数名 ***GeeksforGeeks()。****

```php
*<?php

function GeeksforGeeks() {

    // Magic function constant which
    // holds the function name, or 
    // {closure} for anonymous functions
    $string = __FUNCTION__;

    // Display the result
    echo $string;
}

// Function call
GeeksforGeeks();

?>*
```

***Output:**

```php
GeeksforGeeks

```* 

***程序二:** PHP 程序打印函数**里面的函数名 *Geeks()。****

```php
*<?php

function Geeks() {

    // Magic function constant which
    // holds the class method name
    $string = __METHOD__;

    // Display the result
    echo $string;
}

// Function call
Geeks();

?>*
```

***输出:**

```php
Geeks

```

**参考:***