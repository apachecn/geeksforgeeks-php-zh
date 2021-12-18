# PHP 中的公有、私有、保护有什么区别？

> 原文:[https://www . geesforgeks . org/PHP 中的公共-私有和受保护的区别是什么/](https://www.geeksforgeeks.org/what-is-the-difference-between-public-private-and-protected-in-php/)

公共、私有和受保护的称为访问修饰符。就像 C++一样，PHP 也有公有、私有和受保护三种访问修饰符。属性、方法或常数的可见性可以通过在声明前加上这些关键字来定义。

*   如果类成员声明为公共的，那么它可以在任何地方被访问。
*   如果类成员声明为受保护的，那么它只能在类本身内通过继承子类来访问。
*   如果类成员声明为私有，那么它只能由定义该成员的类访问。

**公共访问修饰符:**这个修饰符在类内外都可以使用。
**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// BaseClass
class pub {
    public $tag_line = "A Computer Science Portal for Geeks!";
    function display() {
        echo $this->tag_line."<br/>";
    }
}

// SubClass
class child extends pub {
    function show(){
        echo $this->tag_line;
    }
}

// Object Declaration
$obj= new child;

// A Computer Science Portal for Geeks!
echo $obj->tag_line."<br/>";

// A Computer Science Portal for Geeks!
$obj->display();

// A Computer Science Portal for Geeks!
$obj->show();
?>
```

**输出:**

```php
A Computer Science Portal for Geeks!
A Computer Science Portal for Geeks!
A Computer Science Portal for Geeks!
```

**受保护访问修饰符:**该修饰符在定义它的类及其父类或继承类中开放使用。
**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Base Class
class pro {
    protected $x = 500;
    protected $y = 500;

    // Subtraction Function
    function sub()
    {
        echo $sum=$this->x-$this->y . "<br/>";
    }    
}

// SubClass - Inherited Class
class child extends pro {
    function mul() //Multiply Function
    {
        echo $sub=$this->x*$this->y;
    }
}

$obj= new child;
$obj->sub();
$obj->mul();
?>
```

**输出:**

```php
0
250000
```

**私有访问修饰符:**这个修饰符在定义它的类中是开放使用的。(不能在类外访问意味着在继承类中)。
**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Base Class
class demo {
    private $name="A Computer Science Portal for Geeks!";

    private function show()
    {
        echo "This is private method of base class";
    }
}

// Sub Class
class child extends demo {
    function display()
    {
        echo $this->name;
    }
}

// Object Declaration
$obj= new child;

// Uncaught Error: Call to private method demo::show()
$obj->show();

//Undefined property: child::$name
$obj->display();
?>
```

**输出:**

```php
It will display error because private class data can not be accessed outside the class
```

**杂例:**
**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
class BaseClass
{
    public $public = 'Public';
    protected $protected = 'Protected';
    private $private = 'Private';

    function Display()
    {
        echo $this->public;
        echo $this->protected;
        echo $this->private;
    }
}

$obj = new BaseClass();
echo $obj->public;
echo $obj->protected; // Cannot access protected property
echo $obj->private; // Cannot access private property
$obj->Display();  //Displays all properties

class SubClass extends BaseClass
{
    public $public = 'Public Sub Class';
    protected $protected = 'Protected Sub Class';

    function Display()
    {
        echo $this->public;
        echo $this->protected;
        echo $this->private;
    }
}

$obj2 = new SubClass();
echo $obj2->public;
echo $obj2->protected; // Cannot access protected property
echo $obj2->private;  // Cannot access private property
$obj2->Display(); //Displays all properties
?>
```

**输出:**

```php
It will display error because private class data can not be accessed outside the class
```

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。