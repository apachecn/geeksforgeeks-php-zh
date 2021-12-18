# PHP 中的抽象类

> 原文:[https://www.geeksforgeeks.org/abstract-classes-in-php/](https://www.geeksforgeeks.org/abstract-classes-in-php/)

抽象类是至少有一个方法是抽象的类。与 C++不同，PHP 中的抽象类是借助抽象关键字来声明的。抽象类的用途是所有实现这个类的基类都应该给出在父类中声明的抽象方法的实现。抽象类可以包含抽象和非抽象方法。

```
<?php

// Abstract class example in PHP
abstract class base
{
    // This is abstract function
    abstract function printdata();

    // This is not abstract function
    function pr()
    {
        echo "Base class";
    }
}
?>
```

下面是一些关于 PHP 中抽象类的重要事实。

*   Like Java, PHP also an instance of abstract class can not be created.

    **示例:**

    ```
    <?php

    // Abstract class
    abstract class Base {
        // This is abstract function
        abstract function printdata();
    }
    class Derived extends base {
        function printdata() {
            echo "Derived class";
        }
    }

    // Uncommenting the following line will 
    // cause compiler error as the line tries
    // to create an instance of abstract class. 
    // $b = new Base(); 

    $b1 = new Derived;
    $b1->printdata();
    ?>
    ```

    **Output:**

    ```
    Derived class

    ```

*   Like C++ or Java abstract class in PHP can contain constructor also.

    **示例:**

    ```
    <?php

    // Abstract class
    abstract class Base {
        function __construct() {
            echo "this is abstract class constructor ";
        }

        // This is abstract function
        abstract function printdata();
    }
    class Derived extends base {
        function __construct() {
            echo "\n Derived class constructor";
        }
        function printdata() {
            echo "\n Derived class printdata function";
        }
    }
    $b1 = new Derived;
    $b1->printdata();
    ?>
    ```

    **Output:**

    ```
    Derived class constructor
     Derived class printdata function

    ```

*   Unlike Java, an abstract class can not be created which does not contains at least one abstract method in PHP. If we run the following example then it will display an error message.

    **示例:**

    ```
    <?php

    // example to understand that an abstract 
    // class can not contain an method with
    // body in php
    abstract class Base {
        abstract function printdata() {
            echo "Parent class printdata";
        }
    }
    ?>
    ```

    **运行时错误:**

    ```
    PHP Fatal error:  Abstract function Base::printdata() cannot contain body 
    in /home/a7540402ade5337d505a779cf4797b38.php on line 7

    ```