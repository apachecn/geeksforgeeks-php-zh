# PHP 中什么是后期静态绑定？

> 原文:[https://www . geesforgeks . org/什么是后期静态绑定 php/](https://www.geeksforgeeks.org/what-is-late-static-bindings-in-php/)

在 PHP 中，程序被保存，然后直接在浏览器上运行，脚本通过网络服务器执行，我们得到输出。我们不会手动编译 PHP 程序，但这并不意味着它永远不会被编译。PHP 解释器会为您完成并运行它。所以有两个阶段，第一，编译时和第二运行时。在编译期间，正常变量被替换为它们的值，但是静态关键字仅在运行时被替换。重写子类中的属性并创建子类的实例，因此为了获得被重写的输出，在使用属性之前，通过编写 static 关键字来使用后期静态绑定概念。每当 PHP 解释器收到编译函数的请求时。如果它看到任何静态属性，那么它让属性在运行时挂起，并且属性在运行时从它被调用的函数中获取它的值。这被称为后期静态绑定。

后期静态绑定的这个特性是在 PHP 5.3 及以上版本中引入的，以前的版本会显示一个致命的错误。

下面的例子说明了 PHP 中的后期静态绑定:

**示例 1:** 在下面的代码中，我们有一个 Car 类及其子类 **newCar** 。每当我们试图通过范围解析操作符(不创建对象)访问 **getOwner()函数**时，我们都会遇到一些问题。两个类都有 **getCar()函数**但是每当我们通过 newCar 类调用 **getOwner()函数**时，它会继承类 Car 中的 **getCar()函数**而不是 newCar。

*   **程序:**在这个程序中我们不会使用静态绑定我们会使用老派的自我，那么你就会得到后期静态绑定的想法。

    ```
    <?php

    // Car function
    class Car
    {
        public static $name = 'Tesla';
        public static function getCar()
        {
            return "The car name is : " . self::$name;
        }
        public static function getOwner()
        {
            echo self::getCar();
        }
    }
    class newCar extends Car
    {

        public static function getCar()
        {

            return "The car name is : " . self::$name . 
                            " and owner is Anshu.";
        }

    }
    Car::getOwner();
    echo "\n";
    newCar::getOwner();

    ?>
    ```

*   **输出:**

    ```
    The car name is : Tesla
    The car name is : Tesla
    ```

*   **程序 2:** 我们可以做的一件事是把 getOwner()函数从 Car 类复制到 **newCar** 类，但是对于小程序来说可以。如果你的程序包含 100 到 1000 个函数呢。为了解决这个问题，可以使用 static 关键字来代替 self。 **newCar** 类不包含 **getOwner()函数**，但仍然继承了 **newCar** 的 **getCar()函数**。之所以会出现这种情况，是因为 **getOwner()** 是在运行时调用 **getCar()** 而不是编译时。Car 类中 **getOwner()函数**的运行时访问，而不是编译或早期访问。这样我们就可以在 **newCar()** 类中得到 **getOwner()** 函数，而不需要创建对象。

    ```
    <?php

    // Car function
    class Car
    {
        public static $name = 'Tesla';
        public static function getCar()
        {
            return "The car name is : " . self::$name;
        }
        public static function getOwner()
        {
            echo static::getCar();
        }
    }
    class newCar extends Car
    {

        public static function getCar()
        {

            return "The car name is : " . self::$name . 
                            " and owner is Anshu.";
        }

    }
    Car::getOwner();
    echo "\n";
    newCar::getOwner();

    ?>
    ```

*   **输出:**

    ```
    The car name is : Tesla
    The car name is : Tesla and owner is Anshu.
    ```

**示例 2:**const 上的后期静态绑定，它将与静态方法一样工作，这意味着它是如何被调用的。对于 const，它不一定是静态的。

*   **程序:**

    ```
    <?php
    class One
    {
        const MY_CONST = false;

        public function selfConst()
        {
            return self::MY_CONST;
        }

        public function staticConst()
        {
            return static ::MY_CONST;
        }
    }

    class Two extends One
    {
        const MY_CONST = true;
    }

    $two = new Two();

    // prints "no"
    echo $two->selfConst() ? 'yes' : 'no';
    echo "\n";

    // prints "yes"
    echo $two->staticConst() ? 'yes' : 'no';
    ?>
    ```

*   **输出:**

    ```
    no 
    yes
    ```

**用在哪里？**

*   其中一个函数被覆盖，您希望显示新的属性。
*   程序太大，你不能一次又一次地写同样的函数。