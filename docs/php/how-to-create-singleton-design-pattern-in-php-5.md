# 如何在 PHP 5 中创建单体设计模式？

> 原文:[https://www . geesforgeks . org/how-create-singleton-design-pattern-in-PHP-5/](https://www.geeksforgeeks.org/how-to-create-singleton-design-pattern-in-php-5/)

当您不想拥有一个给定类的多个实例时，则使用**单例设计模式**，因此名称为–**单例**。Singleton 是 PHP OOPs 概念中的设计模式，是一种只能实例化一次的特殊类。如果该类的对象已经被实例化，那么它将被返回，而不是创建一个新的。
通常在使用各种对象&类时，只定义一次类，然后在我们的应用程序中创建许多对象和实例，每个对象/实例都有自己的属性。例如，当我们有一个名为“学生”的班级名字，它有三个属性——“名字”、“中间名”和“名字”。“学生”的每个实例可能有也可能没有“名字”、“中间名”和“名字”的不同值。但是如果我们使用单例设计模式，那么在程序的给定点上，给定类的实例永远不会超过一个。原因很简单。假设如果我们希望我们的应用程序在数据库中只有一个连接，那么我们必须创建一个名为“DataBase Connector”的单例类，它的工作是确保我们的程序中只有一个数据库连接。这进一步意味着我们可以在全局范围内访问特定的实例，这样我们就不必在函数之间传递数据库连接对象，这样就可以从地球上的每一个地方访问它。
使用 Singleton Design Pattern 的主要原因是我们可以全局使用 Singleton Design Pattern 对象，与其他普通类不同，它只能包含一种对象或一种实例。有时，当有一个像 DataBase 连接一样只创建一次的对象时，使用 Singleton 要好得多。但是请注意，构造函数方法需要是私有的，才能使类成为 Singleton。
下面的程序说明了单例设计模式:
**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

class DataBaseConnector {

    private static $obj;

    private final function __construct() {
        echo __CLASS__ . " initialize only once ";
    }

    public static function getConnect() {
        if (!isset(self::$obj)) {
            self::$obj = new DataBaseConnector();
        }

        return self::$obj;
    }
}

$obj1 = DataBaseConnector::getConnect();
$obj2 = DataBaseConnector::getConnect();

var_dump($obj1 == $obj2);
?>
```

**Output**

```php
DataBaseConnector initialize only once bool(true)

```