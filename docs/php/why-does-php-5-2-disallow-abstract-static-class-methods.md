# PHP 5.2+为什么不允许抽象静态类方法？

> 原文:[https://www . geesforgeks . org/why-do-PHP-5-2-disallow-abstract-static-class-methods/](https://www.geeksforgeeks.org/why-does-php-5-2-disallow-abstract-static-class-methods/)

在我们回答这个问题之前，你必须对什么是抽象类、抽象方法和静态方法有一个清晰的定义。

**抽象类:**在面向对象编程范式中，抽象是指隐藏任何程序的内部实现细节，只向用户展示程序功能的过程。抽象类是实现这一点的一种方式。抽象类是任何不能实例化(即不能创建对象)的类，必须扩展(继承)才能创建对象。“抽象”关键字用于创建抽象类。

**抽象方法:**抽象方法是只能声明而不能定义的方法。它是在继承自这个类别的类别中定义的。

**静态方法:**任何类的静态方法都是只创建一次的方法。这意味着，即使您用静态方法创建了一个类的数百个对象，每个静态方法也只有一个副本。

考虑以下示例:

```
abstract class Abstract_Parent {

    static function X() {
        self::Y();
    }

    abstract static function Y();
}

class Child extends Abstract_Parent {

    static function Y() {
        echo "GeeksforGeeks";
    }
}

Child::X();
```

现在如果运行这个 PHP 代码，就会看到错误，“ *PHP 致命错误:无法调用抽象方法抽象 _Parent::X()* ”

当我们在子类中调用方法 X()时，父类中的静态函数 X()被调用。在方法 X()中，我们再次调用函数 Y()，这是一个 ***抽象静态函数*** 。函数 X()试图调用的 Y()是父类 Y()，它本身就是一个抽象函数。

所以，在同一个方法上使用抽象和静态会破坏彼此的目的。这就是 PHP 5.2+不允许抽象静态类方法的原因。