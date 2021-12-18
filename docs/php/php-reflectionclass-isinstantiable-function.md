# PHP|ReflectionClass isInstantiable()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-isinstantiable-function/](https://www.geeksforgeeks.org/php-reflectionclass-isinstantiable-function/)

**ReflectionClass：：isInstantiable()函数**是 PHP 中的内置函数，用于检查指定的类是否可实例化。

**语法：**

```php
*bool* ReflectionClass::isInstantiable( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果指定的类是可实例化的，则此函数返回 TRUE，否则返回 FALSE。

下面的程序演示了 PHP 中的 ReflectionClass：：isInstantiable()函数：

**程序 1：**

```php
<?php

// Initializing a user-defined Class Departments
class Departments {
    public function CSE() { }
}

// Using ReflectionClass() over the
// user-defined class Departments
$class = new ReflectionClass('Departments');

// Calling the isInstantiable() function
$instance = $class->isInstantiable();

// Getting the value true or false
var_dump($instance);
?>
```

**输出：**

```php
bool(true)

```

**程序 2：**

```php
<?php

// Initializing a interface named as TestFunction
interface TestFunction {
    function F1();
    function F2();
}

// Using ReflectionClass() over the
// specified interface
$class = new ReflectionClass('TestFunction');

// Calling the isInstantiable() function and
// getting the value true or false
var_dump($class->isInstantiable());
?>
```

**输出：**

```php
bool(false)

```

**引用：**[https://www.php.net/manual/en/reflectionclass.isinstantiable.php](https://www.php.net/manual/en/reflectionclass.isinstantiable.php)