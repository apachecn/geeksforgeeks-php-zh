# PHP 中什么时候需要接口？

> 原文:[https://www . geesforgeks . org/when-do-do-we-do-interfaces-in-PHP/](https://www.geeksforgeeks.org/when-do-we-need-interfaces-in-php/)

[接口](https://www.geeksforgeeks.org/php-interface/)是类(实现接口)必须实现的公共 API 的定义。它也被称为契约，因为接口允许指定类必须实现的方法列表。接口定义类似于类定义，只是将关键字 class 改为 Interface。
**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
interface man {

   // List of public methods

}
```

接口可以包含方法和/或常量，但不能包含属性。接口常数与类常数有相同的限制。接口方法是隐式抽象的。
**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

interface IMyInterface {
    const INTERFACE_CONST_1 = 1;
    const INTERFACE_CONST_2 = 'a string';

    public function method_1();
    public function method_2();
}
?>
```

任何需要实现接口的类都必须使用 implements 关键字。一个类一次可以实现多个接口。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
// Function to Implements more than one
// interface by single class.

class MyClass implements IMyInterface {

    public function method_1() {

        // method_1  implementation
    }

    public function method_2() {

        // method_2 implementation
    }
}
```

**有趣点:**

*   一个类不能实现两个具有相同方法名的接口，因为这样会导致方法不明确。
*   像类一样，通过使用同一个关键字“extends”，可以在接口之间建立继承关系。
    **例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
interface Foo {

}
interface Bar {

}
interface Bass extends Foo, Bar {

}
```

下面是一个完整的例子，展示了接口是如何工作的。
**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// PHP program to Implement interface.

// Define a new Interface for all 'shapes'
// to inherit
interface Shape {

    // Define the methods required for
    // classes to implement
    public function getColor();
    public function setColor($color);   

    // Interfaces can't define common
    // functions so we'll just define a
    // method for all implementations to
    // define
    public function describe();
}

// Define a new 'Triangle' class that
// inherits from the 'Shape' interface

class Triangle implements Shape {

    private $color = null;

    // Define the required methods defined
    // in the abstractclass 'Shape'
    public function getColor() {
        return $this->color;
    }  

    public function setColor($color) {
        $this->color = $color;
    }  

    public function describe() {
        return sprintf("GeeksforGeeks %s %s\n",
            $this->getColor(), get_class($this));
    }  
}

$triangle = new Triangle();

// Set the color
$triangle->setColor('green');

// Print out the value of the describe common
// method provided by the abstract class will
// print out out "I am an Orange Triangle"
print $triangle->describe();
?>
```

**输出:**

```php
GeeksforGeeks green Triangle
```

**使用接口的重要性:**

*   接口提供了一个灵活的基/根结构，这是类所没有的。
*   通过实现接口，对象的调用方只需要关心对象的接口，而不需要关心对象方法的实现。
*   接口允许不相关的类实现同一组方法，而不管它们在类继承层次结构中的位置如何。
*   接口使您能够对多重继承进行建模。