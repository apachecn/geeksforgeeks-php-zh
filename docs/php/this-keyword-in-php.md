# $ PHP 中的这个关键词

> 原文:[https://www.geeksforgeeks.org/this-keyword-in-php/](https://www.geeksforgeeks.org/this-keyword-in-php/)

**$this** 是 PHP 中的一个保留关键字，指的是调用对象。它通常是该方法所属的对象，但如果从辅助对象的上下文静态调用该方法，则可能是另一个对象。此关键字仅适用于内部方法。

**示例 1:** 一个简单的程序展示了 *$this* 在 PHP 中的使用。

```php
<?php
class simple{

    public $k = 9;

    public function display(){
        return $this->k;
    }
}

$obj = new simple();
echo $obj->display();

?>
```

**输出:**

```php
9
```

**$ this–伪变量:**与静态、父等类上下文中使用的其他保留关键字不同，不需要用美元符号(' {content} '声明；).这是因为在 PHP 中*$这个*被当作伪变量。
在 PHP 中，这被声明为一个变量声明(带有“{ content }”；符号),即使它是保留关键字。更具体地说，*$这个*是一个特殊的只读变量，它没有在代码的任何地方声明，它代表一个根据程序执行的上下文而变化的值。

**示例 2:** 使用 *$this* 关键字更新特定对象的变量值的程序。

```php
<?php
class simple {

    public $k = 9;

    public function change($val){
        $this->k = $val;
    }

    public function display(){
        return $this->k;
    }
}

$obj = new simple();
print("value of before update: ");
echo $obj->display();

$obj->change(8);
print("value of after update: ");
echo $obj->display();
?>
```

**输出:**

```php
value of before update: 9
value of after update: 8

```

从 PHP 7.0.0 开始，从不兼容的上下文静态调用非静态方法会导致 *$this* 对该方法“未定义”。从 PHP 5.6.0 开始，从不兼容的上下文静态调用非静态方法已被弃用。从 PHP 7.0.0 开始，静态调用非静态方法已被弃用(即使是从兼容的上下文中调用)。在 PHP 5.6.0 之前，这样的调用已经触发了严格的通知。

**示例 3:** 在本例中， *$this* 关键字在静态方法的上下文中调用非静态方法时变为“未定义”。

```php
<?php

class A {

    function foo() {

        if (isset($this)) {
            echo '$this is defined (';
            echo get_class($this);
            echo ")\n";
        } else {
            echo "\$this is not defined.\n";
        }
    }
}

class B {

    function bar() {
        A::foo();
    }
}

$a = new A();
$a->foo();

A::foo();

$b = new B();
$b->bar();

B::bar();
?>
```

**输出:**

```php
$this is defined (A) 
$this is not defined. 
$this is not defined. 
$this is not defined.

```