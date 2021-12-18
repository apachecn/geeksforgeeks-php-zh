# PHP 中的函数重载和覆盖

> 原文:[https://www . geesforgeks . org/function-override-in-PHP/](https://www.geeksforgeeks.org/function-overloading-and-overriding-in-php/)

函数重载和覆盖是 PHP 中的 OOPs 特性。在函数重载中，多个函数可以具有相同的方法签名，但参数数量不同。但是在函数重写的情况下，多个函数将具有相同的方法签名和参数数量。
**函数重载:**函数重载包含相同的函数名，该函数根据参数数量执行不同的任务。例如，找到给定半径的某些形状的面积，那么它应该返回圆的面积。如果给定高度和宽度，那么它应该给出矩形和其他形状的面积。像其他面向对象语言一样，函数重载不能通过本机方法完成。在 PHP 中，函数重载是借助于 magic function __call()完成的。这个函数接受函数名和参数。
**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
// PHP program to explain function
// overloading in PHP

// Creating a class of type shape
class shape {

    // __call is magic function which accepts
    // function name and arguments
    function __call($name_of_function, $arguments) {

        // It will match the function name
        if($name_of_function == 'area') {

            switch (count($arguments)) {

                // If there is only one argument
                // area of circle
                case 1:
                    return 3.14 * $arguments[0];

                // IF two arguments then area is rectangle;
                case 2:
                    return $arguments[0]*$arguments[1];
            }
        }
    }
}

// Declaring a shape type object
$s = new Shape;

// Functio call
echo($s->area(2));
echo "\n";

// calling area method for rectangle
echo ($s->area(4, 2));
?>
```

**Output:** 

```
6.28
8
```

**函数覆盖:**函数覆盖与其他 OOPs 编程语言相同。在函数重写中，父类和子类应该具有相同的函数名和参数个数。它用于替换子类中的父方法。重写的目的是改变父类方法的行为。具有相同名称和参数的两个方法称为重写。
**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
// PHP program to implement
// function overriding

// This is parent class
class P {

    // Function geeks of parent class
    function geeks() {
        echo "Parent";
    }
}

// This is child class
class C extends P {

    // Overriding geeks method
    function geeks() {
        echo "\nChild";
    }
}

// Reference type of parent
$p = new P;

// Reference type of child
$c= new C;

// print Parent
$p->geeks();

// Print child
$c->geeks();
?>
```

**Output:** 

```
Parent
Child
```

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。