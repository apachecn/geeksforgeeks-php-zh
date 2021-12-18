# PHP 中的特性与接口

> 原文:[https://www.geeksforgeeks.org/traits-vs-interfaces-in-php/](https://www.geeksforgeeks.org/traits-vs-interfaces-in-php/)

PHP 中的 traits 和 Interfaces 的主要区别在于 Traits 定义了每个类中每个方法的实际实现，因此许多类实现了相同的接口但具有不同的行为，而 Traits 只是 PHP 中注入到一个类中的代码块。

**性状**

特质根本不是界面。特性可以定义静态成员和静态方法。它帮助开发人员在不同类层次的几个独立类中自由重用方法。特性降低了复杂性，并避免了与多重继承和混合相关的问题。注意 PHP 不允许多重继承。因此，通过允许我们在多个类中重用相同的功能，Traits 被用来填补这个空白。

**语法:**

```
<?php
// A sample trait in PHP
trait namethis {
    function ReturnType() {  }
    function ReturnDescription() {  }
}?>
```

特征不能实现接口。一个特性允许两个类将它用于公共接口需求。它支持使用抽象方法。它支持对传统继承行为的横向组合。特性是单继承语言(如 PHP)中代码重用的一种机制。再次编写相同的代码，以避免使用特征。当多个类共享相同的功能时，使用这些特性。

**示例:**

```
<?php
// PHP program to demonstrate working
// of trait.
trait HelloGeeks {
    public function geeks() {
        echo 'Hello World!';
    }
}

class Geeksforgeeks {
    use HelloGeeks;
    public function geeks() {
        echo 'Hello Geeks!';
    }
}

$obj = new Geeksforgeeks();
$obj->geeks();
?>
```

**输出:**

```
Hello Geeks!
```

**界面**

它指定了类必须实现的所有此类方法的列表。使用关键字*接口*实现与类相同的接口。它可以使用 extends 运算符扩展接口。Interface 中的所有方法都是抽象方法，可以有自己的常量。有一个具体的类概念，它是一个实现接口的类，该接口必须实现所有具有相同名称和签名的方法。
界面中的所有方法必须具有公共访问级别。

**语法:**

```
<?php
// A sample interface in PHP
interface MyInterface
{
 // function...
}
```

没有两个接口可以由具有相同方法名和签名的特定类实现，因为它会产生错误。还有助于多重继承，因为一个类可以实现多个接口，而它只能扩展一个类。可以在不影响接口调用方的情况下更改实现。

**示例:**

```
<?php 
// PHP program to demonstrate working
// of interface.
interface MyInterface{ 

    public function examplemethod1(); 
    public function examplemethod2(); 

} 

class MyClass implements MyInterface{ 

    public function examplemethod1(){ 
        echo "ExampleMethod1 Called" . "\n"; 
    } 

    public function examplemethod2(){ 
        echo "ExampleMethod2 Called". "\n"; 
    } 
} 

$ob = new MyClass; 
$ob->examplemethod1(); 
$ob->examplemethod2(); 

?> 
```

**输出:**

```
ExampleMethod1 Called
ExampleMethod2 Called

```