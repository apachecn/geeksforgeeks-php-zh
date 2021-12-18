# PHP|ReflectionClass getStaticPropertyValue()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-getstaticpropertyvalue-function/](https://www.geeksforgeeks.org/php-reflectionclass-getstaticpropertyvalue-function/)

**ReflectionClass：：getStaticPropertyValue()函数**是 PHP 中的内置函数，用于返回静态属性的值。

**语法：**

```php
*mixed* ReflectionClass::getStaticPropertyValue( *string* $name, *mixed* &$def_value )
```

**参数：**此函数接受单个参数**名称**，它是指定的静态属性的名称。

**返回值：**此函数返回静态属性的值。

下面的程序演示了 PHP 中的 ReflectionClass：：getStaticPropertyValue()函数：

**程序 1：**

```php
<?php

// Defining a class named as Departments
class Departments {
    static $Dept1 = 'CSE';
    private static $Dept2 = 'ECE';
    public static $Dept3 = 'EE';
}

// Using ReflectionClass over the class Departments
$ReflectionClass = new ReflectionClass('Departments');

// Calling getStaticPropertyValue() function
$A = $ReflectionClass->getStaticPropertyValue('Dept3');

// Getting the value of the static property.
var_dump($A);
?>
```

**输出：**

```php
string(2) "EE"

```

**程序 2：**

```php
<?php

// Defining a class named as Departments
class Departments {
    static $Dept1 = 'CSE';
    static $Dept2 = 'ECE';
    public static $Dept3 = 'EE';
}

// Using ReflectionClass over the class Departments
$ReflectionClass = new ReflectionClass('Departments');

// Calling getStaticPropertyValue() functions
$A = $ReflectionClass->getStaticPropertyValue('Dept1');
$B = $ReflectionClass->getStaticPropertyValue('Dept2');
$C = $ReflectionClass->getStaticPropertyValue('Dept3');

// Getting the value of the static property.
var_dump($A);
var_dump($B);
var_dump($C);
?>
```

**输出：**

```php
string(3) "CSE"
string(3) "ECE"
string(2) "EE"

```

**引用：**[https://www.php.net/manual/en/reflectionclass.getstaticpropertyvalue.php](https://www.php.net/manual/en/reflectionclass.getstaticpropertyvalue.php)