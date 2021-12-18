# PHP 中新自我对新静态

> 原文:[https://www . geesforgeks . org/new-self-vs-new-static-in-PHP/](https://www.geeksforgeeks.org/new-self-vs-new-static-in-php/)

**新自我:**自我是 PHP 中的关键词。它指的是实际写入新关键字的同一个类。它引用类成员，但不引用任何特定对象。这是因为静态成员(变量或函数)是由类的所有对象共享的类成员。名为**self::function()**的函数的行为类似于“我将在我实际所属的类的上下文中执行。”(假设继承场景)。

*   **示例:**假设我们对 Car 类中的静态模型函数进行了这样的调用——由于它是一个静态函数，我们当然可以仅使用类名

    ```
    <?php
    class Car
    {
        public static function model()
        {
            self::getModel();
        }

        protected static function getModel()
        {
            echo "I am a Car!";
        }

    }

    class Mercedes extends Car
    {

        protected static function getModel()
     {
            echo "I am a Mercedes!";
        }

    }
    Car::model();
    echo("\n");
    Mercedes::model();
    ?>
    ```

    直接调用该函数
*   **输出:**

    ```
    I am a Car!
    I am a Car!
    ```

*   **Explanation:** The model function is defined inside the Car class, and it is not overridden by the Mercedes class– but the model function is of course inherited by the Mercedes class.
    As a result, when we call the version of the model inside the Mercedes class, the scope of the function is still inside the Car class– because the function definition is inside the Car class. The way the keyword **“self”** works are that it will call the current class’s implementation of the getModel function – and since the model function is defined inside the Car class, the current class would be the Car class.

    所以，它将调用 **getModel** 的 Car 类实现，而不是 Mercedes 类实现。这种行为可能被认为是不可取的，因为它不是多态的，并且不符合面向对象的设计原则。但是，有一个替代解决方案可以让我们获得这种行为——这就是静态关键字变得有用的地方。

**New static:**static 是 PHP 中的一个关键字。在 PHP 5.3 的后期静态绑定中，Static 指的是层次结构中调用方法的任何类。静态最常见的用法是定义静态方法。这种方法是类的一部分，就像任何方法一样，尽管它们可以在没有任何这种实例化对象的情况下使用。被调用的函数**static::fFunction()**的行为类似于“我将在类的上下文中执行，这个类实际上已经被外界调用了”。

*   **例:**

    ```
    <?php
    class Car
    {
        public static function model()
        {
             static::getModel();
        }

        protected static function getModel()
        {
            echo "I am a Car!";
        }
    }

    class Mercedes extends Car
    {

        protected static function getModel()
     {
            echo "I am a Mercedes!";
        }

    }
    Car::model();
    echo("\n");
    Mercedes::model();
    ?>
    ```

*   **输出:**

    ```
    I am a Car!
    I am a Mercedes!
    ```

**PHP new self vs new static:** 现在我们将示例中的代码改为使用 static 而不是 self，您可以看到不同之处在于 self 引用了当前类，而 static 关键字允许函数在运行时绑定到调用类。自我和静态关键词的区别用一个例子就相当容易理解了。

```
<?php
class g {

    /* The new self */
    public static function get_self() {
    return new self();
    }

    /* The new static */
    public static function get_static() {
    return new static();
    }
}

class f extends g {}

echo get_class(f::get_self()); // g
echo get_class(f::get_static()); // f
echo get_class(g::get_self()); // g
?>
```

**输出:**在这个代码示例中，f 继承了 g 的两个方法。自调用绑定到 A，因为它是在 g 的方法实现中定义的，而静态绑定到被调用的类。

```
gfg
```