# PHP|ReflectionClass getProperties()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-getproperties-function/](https://www.geeksforgeeks.org/php-reflectionclass-getproperties-function/)

**ReflectionClass：：getProperties()函数**是 PHP 中的内置函数，用于返回反射属性的数组。

**语法：**

```php
ReflectionClass::getProperties($filter) : array
```

**参数：**此函数接受参数**filter**，该参数有助于删除某些反射的属性。

**返回值：**此函数返回反映的属性数组。

以下程序说明 PHP：
**程序 1：**中的 ReflectionClass：：getProperties()函数

```php
<?php

// Defining a class named as Departments
class Departments {
    public $Dept1 = 'CSE';
    private $Dept2 = 'ECE';
    public static $Dept3 = 'EE';
}

// Using ReflectionClass over the class Departments
$ReflectionClass = new ReflectionClass('Departments');

// Calling getProperties() function over a filter called 
// ReflectionProperty::IS_PUBLIC which  
// will reflect results of only public properties
$A = $ReflectionClass->getProperties(ReflectionProperty::IS_PUBLIC);

// Getting an array of the reflected properties
var_dump($A);
?>
```

发帖主题：Re：Колибри0.7.0

```php
array(2) {
  [0]=>
  object(ReflectionProperty)#2 (2) {
    ["name"]=>
    string(5) "Dept1"
    ["class"]=>
    string(11) "Departments"
  }
  [1]=>
  object(ReflectionProperty)#3 (2) {
    ["name"]=>
    string(5) "Dept3"
    ["class"]=>
    string(11) "Departments"
  }
}

```

**程序 2：**

```php
<?php

// Defining a class named as Company
class Company {
    public $C1;
    private $C2;
    public static $C3;
}

// Using ReflectionClass over the class Company
$ReflectionClass = new ReflectionClass('Company');

// Calling getProperties() function without
// of any filter
$A = $ReflectionClass->getProperties();

// Getting an array of the reflected properties
var_dump($A);
?>
```

**Output:**

```php
array(3) {
  [0]=>
  object(ReflectionProperty)#2 (2) {
    ["name"]=>
    string(2) "C1"
    ["class"]=>
    string(7) "Company"
  }
  [1]=>
  object(ReflectionProperty)#3 (2) {
    ["name"]=>
    string(2) "C2"
    ["class"]=>
    string(7) "Company"
  }
  [2]=>
  object(ReflectionProperty)#4 (2) {
    ["name"]=>
    string(2) "C3"
    ["class"]=>
    string(7) "Company"
  }
}

```

**引用：**[https://www.php.net/manual/en/reflectionclass.getproperties.php](https://www.php.net/manual/en/reflectionclass.getproperties.php)