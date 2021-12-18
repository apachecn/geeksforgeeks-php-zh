# 自我:$bar 和静态:$bar 在 PHP 中的区别

> 原文:[https://www . geeksforgeeks . org/PHP 中 selfbar 和 staticbar 的区别/](https://www.geeksforgeeks.org/difference-between-selfbar-and-staticbar-in-php/)

***self* 关键字:**它是一个 PHP 关键字，表示当前类，用于访问静态类变量或静态变量，因为这些成员属于一个类，而不是该类的对象。

**例:**

```
<?php

// Declaring parent class
class demo {

    public static $bar = 10;

    public static function func() {
        echo self::$bar . "\n";
    }
}

// Declaring child class
class Child extends demo {
    public static $bar = 20;

}

// Calling for demo's 
// version of func()
demo::func();

// Calling for child's 
// version of func()
Child::func();

?>
```

**输出:**

```
10
10

```

您可以看到，在这两种情况下,$bar 的值都打印在演示类中，尽管在第二次调用中，我们试图获取子类的$bar 的值。发生这种情况是因为' self '关键字。Self 仅指$bar 的编译时版本，或者更简单地说，是指它所在的类的版本。事实上，它被认为是对“自我”的限制，但可以通过使用“静态”关键字来修复。

***Static* 关键字:**这个 PHP 关键字帮助“PHP 中后期静态绑定”的概念出现在图片中。它用于在运行时访问扩展类所需的静态函数。

**例:**

```
<?php

// Declaring parent class
class demo {

    public static $bar = 10;

    public static function func() {

        // Static in place of self
        echo static::$bar."\n";
    }
}

// Declaring child class
class Child extends demo {
    public static $bar = 20;
}

// Calling for demo's version of func()
demo::func();

// Calling for child's version of func()
Child::func();

?>
```

**输出:**

```
10
20

```

“static”关键字通过强制执行后期静态绑定的概念来覆盖“self”关键字的限制。在这种情况下，static 要求编译器打印请求它的类的函数版本。所有这些都发生在运行时，因此后期静态绑定是在 PHP 运行时显示多态性的一种方式。

**self Vs static:** 它们之间最基本的区别是 self 指向声明它的类的属性的版本，但是在 static 的情况下，属性在运行时会经历重新声明。