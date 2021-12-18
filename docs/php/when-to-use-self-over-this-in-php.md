# PHP 中什么时候使用 self over $this？

> 原文:[https://www . geesforgeks . org/何时使用-php 中的自我超越/](https://www.geeksforgeeks.org/when-to-use-self-over-this-in-php/)

**自身**和**这个**是两个不同的运算符，分别用来表示当前类和当前对象。self 用于访问静态或类变量或方法，而这用于访问非静态或对象变量或方法。
所以当需要访问属于一个类的东西时使用 self，当需要访问属于该类的对象的属性时使用$this。
**self 运算符:** self 运算符代表当前类，因此用于访问类变量或静态变量，因为这些成员属于某个类，而不是该类的对象。
**语法:**

```
self::$static_member
```

**例 1:** 这是展示 self 运算符使用的基本示例。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

class GFG {
    private static $static_member = "GeeksForGeeks";

    function __construct() {
        echo self::$static_member;
        // Accessing static variable
    }
}

new GFG();
?>
```

**输出:**

```
GeeksForGeeks
```

**示例 2:** 这个示例是使用 self 在 php 中开发多态行为的演示。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

class GFG {
    function print() {
        echo 'Parent Class';
    }

    function bar() {
        self::print();
    }
}

class Child extends GFG {
    function print() {
        echo 'Child Class';
    }
}

$parent = new Child();
$parent->bar();
?>
```

**输出:**

```
Parent Class:
```

这里运行父类方法是因为 self 操作符代表类，因此我们看到主类方法只是父类的方法。
**$本符:**$本，为' {content} '号；暗号暗示，是一个物体。$这表示类的当前对象。它用于访问类的非静态成员。
**语法:**

```
$that->$non_static_member;
```

**示例 1:** 这是显示使用$this 运算符的基本示例。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
class GFG {
    private $non_static_member = "GeeksForGeeks";

    function __construct() {
        echo $this->$non_static_member;
        // accessing non-static variable
    }
}

new GFG();
?>
```

**输出:**

```
GeeksForGeeks
```

**示例 2:** 这个示例是 php 中使用 self 的多态行为的演示。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

class GFG {
    function print() {
        echo 'Parent Class';
    }

    function bar() {
        $this->print();
    }
}

class Child extends GFG {
    function print() {
        echo 'Child Class';
    }
}

$parent = new Child();
$parent->bar();
?>
```

**输出:**

```
Child Class
```

这里没有对任何类的引用，指向子类的对象正在调用子类中定义的方法。这是 PHP 中动态多态的一个例子。