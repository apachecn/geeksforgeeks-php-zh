# 什么是神奇的方法，如何在 PHP 中使用？

> 原文:[https://www . geesforgeks . org/什么是神奇的方法以及如何在 php 中使用它们/](https://www.geeksforgeeks.org/what-are-magic-methods-and-how-to-use-them-in-php/)

PHP 魔术方法是特殊的方法，当满足某些条件时会自动调用。PHP 中有几种神奇的方法。每种神奇的方法都遵循一定的规则–

*   每个神奇的方法都以双下划线(__)开头。
*   它们是预定义的，既不能创建也不能删除。
*   魔法方法有保留的名字，它们的名字不应该用于其他目的。
*   当满足某些条件时，会自动调用魔术方法。

<figure class="table">

| **方法名称** | **返回类型** | **通话条件** |
| _ _ 构造() | 圆盘烤饼 | 每当创建特定类的对象时，都会自动调用此方法。这种神奇方法的功能与任何 OOP 语言中的构造函数相同。 |
| _ _ 销毁() | 圆盘烤饼 | 顾名思义，当对象被破坏并且不再使用时，就调用这个方法。一般在程序的末尾和函数的末尾。

 |
| __call($name，$parameter) | 不是强制性的 | 当调用尚未定义的方法时，此方法执行。 |
| __toString() | 线 | 当我们需要将对象转换成字符串时，就会调用这个方法。例如:echo $ obj$ obj-> _ _ ToString()；会被神奇地调用。 |
| __get($name) | 圆盘烤饼 | 当使用不可访问的变量或不存在的变量时，调用此方法。 |
| _ _ 套($name，$value) | 圆盘烤饼 | 当写入不可访问的变量或不存在的变量时，将调用此方法。 |
| _ _ _ debug info() | 排列 | 当在 var_dump()中使用对象进行调试时，会执行这个神奇的方法。 |

</figure>

下面是一些代码片段和例子来更好地理解神奇的方法。

**__construct()方法:**在下面的示例中，magic method 类有一个神奇的方法 **__construct()** ，每次创建 MagicMethod 类的新对象时都会调用它。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

class MagicMethod {
    function __construct() {
        echo "This is the construct magic method";
    }
}

// Creating object of Magic method class
$obj = new MagicMethod();

?>
```

**Output**

```php
This is the construct magic method
```

**_ _ destrude()方法:**在下面的例子中，magic method 类有一个魔法方法**_ _ destrude()**，当 MagicMethod 的对象破坏时，它会被自动调用。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

class MagicMethod {
    function __destruct() {
        echo "This destruct magic method "
        + "gets called when object destroys";
    }
}

$obj = new MagicMethod();

?>
```

**Output**

```php
This destruct magic method gets called 
when object destroys
```