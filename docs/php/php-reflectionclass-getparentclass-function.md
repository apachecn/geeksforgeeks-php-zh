# PHP|ReflectionClass getParentClass()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-getparentclass-function/](https://www.geeksforgeeks.org/php-reflectionclass-getparentclass-function/)

**ReflectionClass：：getParentClass()函数**是 PHP 中的一个内置函数，用于返回指定的父类，如果没有父类，则返回 False。

**语法：**

```php
*ReflectionClass* ReflectionClass::getParentClass ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定的父类，如果没有父类，则返回 False。

以下程序说明 PHP：
**程序 1：**中的**ReflectionClass：：getParentClass()**函数

```php
<?php

// Defining a class named as College
class College {

    // Defining a protected property
    protected $College_Name = 'IIT Delhi';
}

// Defining a sub class Departments of the 
// base class College
class Departments extends College {
    public $Dept1 = 'CSE';
    private $Dept2 = 'ECE';
    public static $Dept3 = 'EE';
}

// Using ReflectionClass over sub class Departments
$ReflectionClass = new ReflectionClass('Departments');

// Getting the name of the parent class
var_dump($ReflectionClass->getParentClass());
?>
```

发帖主题：Re：Колибри0.7.0

```php
object(ReflectionClass)#2 (1) {
  ["name"]=>
  string(7) "College"
}

```

**程序 2：**

```php
<?php

// Defining a class named as College
class College {

    // Defining a protected property
    protected $College_Name = 'IIT Delhi';
}

// Using ReflectionClass over the class College
$ReflectionClass = new ReflectionClass('College');

// Getting the name of the parent class
var_dump($ReflectionClass->getParentClass());
?>
```

发帖主题：Re：Колибри0.7.0

```php
bool(false)

```

**引用：**[https://www.php.net/manual/en/reflectionclass.getparentclass.php](https://www.php.net/manual/en/reflectionclass.getparentclass.php)