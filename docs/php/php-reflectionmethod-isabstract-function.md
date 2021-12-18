# PHP|ReflectionMethod isAbstract()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionmethod-isabstract-function/](https://www.geeksforgeeks.org/php-reflectionmethod-isabstract-function/)

**ReflectionMethod：：isAbstract()函数**是 PHP 中的一个内置函数，用于在指定的方法是抽象的时返回 true，否则返回 false。

**语法：**

```
*bool* ReflectionMethod::isAbstract ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果指定的方法是抽象的，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明 PHP：
**Program_1：**中的**ReflectionMethod：：isAbstract()函数**

```
<?php

// Initializing a user-defined abstract class
abstract class Company {

    abstract function GFG();
}

// Using ReflectionMethod() over the class Company
$A = new ReflectionMethod('Company', 'GFG');

// Calling the isAbstract() function
$B = $A->isAbstract();

// Getting the value TRUE if the specified
// method is abstract, otherwise FALSE.
var_dump($B);
?>
```

发帖主题：Re：Колибри0.7.0

```
bool(true)

```

**程序 _2：**

```
<?php

// Initializing some user-defined classes
class Department1 {

    public function hr($name) {
        return 'HR' . $name;
    }
}
class Department2 {

    public function coding($name) {
        return 'Coding' . $name;
    }
}
abstract class Department3 {

    abstract function marketing();
}

// Using ReflectionMethod() over the above classes
$A = new ReflectionMethod('Department1', 'hR');
$B = new ReflectionMethod('Department2', 'coding');
$C = new ReflectionMethod('Department3', 'marketing');

// Calling the isAbstract() function and 
// getting the value TRUE if the specified
// method is abstract, otherwise FALSE.
var_dump($A->isAbstract());
var_dump($B->isAbstract());
var_dump($C->isAbstract());
?>
```

发帖主题：Re：Колибри0.7.0

```
bool(false)
bool(false)
bool(true)

```

**引用：**[https://www.php.net/manual/en/reflectionmethod.isabstract.php](https://www.php.net/manual/en/reflectionmethod.isabstract.php)