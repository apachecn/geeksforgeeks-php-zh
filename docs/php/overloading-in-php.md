# PHP 中的重载

> 原文:[https://www.geeksforgeeks.org/overloading-in-php/](https://www.geeksforgeeks.org/overloading-in-php/)

**什么是函数重载？**
函数重载是用不同的实现创建多个同名函数的能力。

**PHP 中的函数重载？**
PHP 中的函数重载用于动态创建属性和方法。这些动态实体由魔术方法处理，这些方法可以在一个类中用于各种动作类型。函数重载包含相同的函数名，并且该函数根据参数的数量执行不同的任务。例如，找到给定半径的某些形状的面积，那么它应该返回圆的面积。如果给定高度和宽度，那么它应该给出矩形和其他形状的面积。像其他面向对象语言一样，函数重载不能通过本机方法完成。在 PHP 中，函数重载是借助于 magic function __call()完成的。这个函数接受函数名和参数。

**PHP 中重载的属性和规则:**

*   所有重载方法都必须定义为 Public。
*   为类创建对象后，我们可以访问一组实体，这些实体是类范围内未定义的属性或方法。
*   这种实体被称为重载属性或方法，这个过程被称为重载。
*   为了处理这些重载的属性或函数，使用了 PHP 魔法方法。
*   除了在静态上下文中使用的 __callStatic()方法之外，大多数神奇的方法都将在对象上下文中触发。

**PHP 中的重载类型:**PHP 中有两种类型的重载。

*   属性重载
*   方法重载

**属性重载:** PHP 属性重载用于在对象上下文中创建动态属性。创建这些属性不需要单独的代码行。与类实例关联的属性，如果它没有在类的范围内声明，则被视为重载属性。
下面的操作是用 PHP 中的重载属性执行的。

*   设置和获取重载属性。
*   评估重载属性设置。
*   撤消此类属性设置。

在执行操作之前，我们应该定义适当的魔术方法。它们是，

*   **__set():** 初始化重载属性时触发。
*   **__get():** 在 PHP 打印语句中使用重载属性时触发。
*   **__isset():** 当我们用 isset()函数检查重载属性时，调用这个神奇的方法
*   **__unset():** 同样，对于重载属性，在使用 PHP unset()时将调用此函数。

**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// 
class GFG {

    // Location of overloading data
    private $data = array();

    // Overloading not used here
    public $declared = 1;

    // Overloading used when accessed
    // outside the class
    private $hidden = 2;

    // Function definition
    public function __set($name, $value) {
        echo "Setting '$name' to '$value'\n";
        $this->data[$name] = $value;
    }

    // Function definition
    public function __get($name) {
        echo "Getting '$name: ";
        if (array_key_exists($name, $this->data)) {
            return $this->data[$name];
        }

        $trace = debug_backtrace();

        return null;
    }

    // Function definition
    public function __isset($name) {
        echo "Is '$name' set?\n";
        return isset($this->data[$name]);
    }

    // Definition of __unset function
    public function __unset($name) {
        echo "Unsetting '$name'\n";
        unset($this->data[$name]);
    }

    // getHidden function definition
    public function getHidden() {
        return $this->hidden;
    }
}

// Create an object
$obj = new GFG;

// Set value 1 to the object variable
$obj->a = 1;
echo $obj->a . "\n";

// Use isset function to check
// 'a' is set or not
var_dump(isset($obj->a));

// Unset 'a'
unset($obj->a);

var_dump(isset($obj->a));

echo $obj->declared . "\n\n";

echo "Private property are visible inside the class ";
echo $obj->getHidden() . "\n\n";

echo "Private property are not visible outside of class\n";
echo $obj->hidden . "\n";

?>
```

**Output:**

```php
Setting 'a' to '1'
Getting 'a: 1
Is 'a' set?
bool(true)
Unsetting 'a'
Is 'a' set?
bool(false)
1

Private property are visible inside the class 2

Private property are not visible outside of class
Getting 'hidden:

```

**方法重载:**这是一种重载类型，用于创建未在类范围内声明的动态方法。PHP 方法重载还会触发专用于适当目的的神奇方法。与属性重载不同，PHP 方法重载允许对对象和静态上下文进行函数调用。
相关的魔法功能有，

*   _ _ call()–在对象上下文中调用重载方法时触发。
*   _ _ callStatic()–在静态上下文中调用重载方法时触发。

**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
class GFG {

    public function __call($name, $arguments) {

        echo "Calling object method '$name' "
            . implode(', ', $arguments). "\n";
    }

    public static function __callStatic($name, $arguments) {

        echo "Calling static method '$name' "
            . implode(', ', $arguments). "\n";
    }
}

// Create new object
$obj = new GFG;

$obj->runTest('in object context');

GFG::runTest('in static context'); 

?>
```

**Output:**

```php
Calling object method 'runTest' in object context
Calling static method 'runTest' in static context

```