# PHP|ReflectionClass getExtension()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-getextension-function/](https://www.geeksforgeeks.org/php-reflectionclass-getextension-function/)

**ReflectionClass：：getExtension()函数**是 PHP 中的一个内置函数，用于返回 ReflectionExtension 对象，该对象表示已定义类的扩展，或者对于用户定义的类为 NULL。

**语法：**

```php
*ReflectionExtension* ReflectionClass::getExtension( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回 ReflectionExtension 对象，该对象表示已定义类的扩展，或者对于用户定义的类返回 NULL。

下面的程序演示了 PHP 中的 ReflectionClass：：getExtension()函数：

**程序 1：**

```php
<?php

// Defining a user-defined class named as Departments
class Departments {
    static $Dept1 = 'CSE';
    private static $Dept2 = 'ECE';
    public static $Dept3 = 'EE';
}

// Using ReflectionClass over the class Departments
$ReflectionClass = new ReflectionClass('Departments');

// Calling getExtension() functions
$A = $ReflectionClass->getExtension();

// Getting the ReflectionExtension object
var_dump($A);
?>
```

**输出：**

```php
NULL

```

**程序 2：**

```php
<?php

// Using ReflectionClass
$ReflectionClass = new ReflectionClass('ReflectionClass');

// Calling getExtension() functions
$A = $ReflectionClass->getExtension();

// Getting the ReflectionExtension object
var_dump($A);
?>
```

**输出：**

```php
object(ReflectionExtension)#2 (1) {
  ["name"]=>
  string(10) "Reflection"
}

```

**引用：**[https://www.php.net/manual/en/reflectionclass.getextension.php](https://www.php.net/manual/en/reflectionclass.getextension.php)