# PHP 中如何实现方法重载？

> 原文:[https://www . geeksforgeeks . org/如何实现方法-php 中的重载/](https://www.geeksforgeeks.org/how-to-implement-method-overloading-in-php/)

PHP 代表超文本预处理器，它是一种流行的通用脚本语言，主要用于网络开发。它快速、灵活、实用，PHP 的最新版本是面向对象的，这意味着您可以编写类，使用继承、多态性、数据抽象、封装、构造函数、析构函数以及重载(方法和函数)。

[**重载**](https://www.geeksforgeeks.org/overloading-in-php/) **:** 重载是一个面向对象的概念，其中两个或多个方法具有相同的方法名，但具有不同的参数或参数(强制的)和返回类型(不必要)。可以通过构造函数重载、运算符重载和方法重载来实现。
在本文中，我们将在 PHP 中实现方法重载。

**PHP 中的方法重载:**

**示例:**下面给出的代码将显示一些错误。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

class GFG {
    function multiply($var1){
        return $var1;
    }

    function multiply($var1,$var2){
        return $var1 * $var1 ;
    }
}

$ob = new GFG();
$ob->multiply(3,6);
?>
```