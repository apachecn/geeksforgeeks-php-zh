# PHP 中的最终关键字

> 原文:[https://www.geeksforgeeks.org/final-keyword-in-php/](https://www.geeksforgeeks.org/final-keyword-in-php/)

PHP 中的 Final 关键字在不同的上下文中使用。final 关键字仅用于方法和类。
![final keyword](img/a6ec137455438daa11ce4c6d389a5fe4.png)
**最终方法:**当一个方法被声明为最终方法时，不能对该方法进行覆盖。由于某些设计原因，方法被声明为最终方法。方法不应因安全或任何其他原因而被重写。

**示例:**

```
<?php

// Program to understand use of 
// final keyword for methods
class Base {

    // Final method
    final function printdata() {
        echo " Base class final printdata function";
    }

    // Non final method
    function nonfinal() {
        echo "\n This is nonfinal function of base class";
    }
}

// Class that extend base class
class Derived extends Base {

    // Inheriting method nonfinal 
    function nonfinal() {
        echo "\n Derived class non final function";
    }

    // Here printdata function can
    // not be overridden
}

$obj = new Derived;
$obj->printdata();
$obj->nonfinal();
?>
```

**Output:**

```
Base class final printdata function
 Derived class non final function

```

**终级类:**声明为终级的类以后不能扩展。由于一些设计级别的问题，类被声明为最终类。如果类创建者希望该类由于某种安全或其他原因不被继承，那么他就将该类声明为最终类。最终类可以包含最终和非最终方法。但是当类本身被声明为 final 时，在类中没有 final 方法的使用，因为继承是不可能的。

**示例:**

```
<?php

// Program to understand final classes
// in php
final class Base {

    // Final method
    final function printdata() {
        echo "final base class final method";
    }

    // Non final method
    function nonfinal() {
        echo "\nnon final method of final base class";
    }
}

$obj = new Base;
$obj->printdata();
$obj->nonfinal();

/* If we uncomment these lines then it will
show Class Derived may not inherit from final
class (Base)
class Derived extends Base {

} */
?>
```

**Output:**

```
final base class final method
non final method of final base class

```

**注意:**不像 PHP 中的 Java final 关键字只能用于方法和类，不能用于变量。