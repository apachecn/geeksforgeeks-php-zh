# PHP|ReflectionClass isInterface()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-isinterface-function/](https://www.geeksforgeeks.org/php-reflectionclass-isinterface-function/)

**ReflectionClass：：isInterface()函数**是 PHP 中的内置函数，用于检查指定的类是否为接口。

**语法：**

```php
*bool* ReflectionClass::isInterface( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果指定的类是接口，则此函数返回 TRUE，否则返回 FALSE。

下面的程序演示了 PHP 中的 ReflectionClass：：isInterface()函数：

**程序 1：**

```php
<?php

// Initializing a user-defined interface Departments
interface Departments {
    public function CSE();
}

// Using ReflectionClass() over the
// user-defined interface Departments
$class = new ReflectionClass('Departments');

// Calling the isInterface() function
$instance = $class->isInterface();

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

// Initializing a user-defined class TestInterface
Class TestInterface {
}

// Using ReflectionClass() over the
// user-defined class TestInterface
$class = new ReflectionClass('TestInterface');

// Calling the isInterface() function and
// getting the value true or false
var_dump($class->isInterface());
?>
```

**输出：**

```php
bool(false)

```

**引用：**[https://www.php.net/manual/en/reflectionclass.isinterface.php](https://www.php.net/manual/en/reflectionclass.isinterface.php)