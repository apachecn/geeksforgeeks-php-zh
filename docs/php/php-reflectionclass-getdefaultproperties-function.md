# PHP|ReflectionClass getDefaultProperties()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-getdefaultproperties-function/](https://www.geeksforgeeks.org/php-reflectionclass-getdefaultproperties-function/)

**ReflectionClass：：getDefaultProperties()函数**是 PHP 中的内置函数，用于返回默认属性，包括从指定类继承的属性。

**语法：**

```
ReflectionClass::getDefaultProperties(void) : array
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回默认属性数组。 这些属性为属性的键及其值提供了空间。 键是属性的名称，值是属性的默认值。 如果属性没有任何默认值，它也返回 NULL。

以下程序说明 PHP：
**程序 1：**中的 ReflectionClass：：getDefaultProperties()函数

```
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

// Getting an array of the default properties
var_dump($ReflectionClass->getDefaultProperties());
?>
```

发帖主题：Re：Колибри0.7.0

```
array(4) {
  ["Dept3"]=>
  string(2) "EE"
  ["Dept1"]=>
  string(3) "CSE"
  ["Dept2"]=>
  string(3) "ECE"
  ["College_Name"]=>
  string(9) "IIT Delhi"
}

```

**程序 2：**

```
<?php

// Defining a class named as College
class College {

    // Defining a protected property
    protected $College_Name = 'IIT Delhi';
}

// Defining a sub class Departments of the 
// base class College
class Departments extends College {
    public $Dept1;
    private $Dept2;
    public static $Dept3;
}

// Using ReflectionClass over sub class Departments
$ReflectionClass = new ReflectionClass('Departments');

// Getting an array of the default properties
var_dump($ReflectionClass->getDefaultProperties());
?>
```

发帖主题：Re：Колибри0.7.0

```
array(4) {
  ["Dept3"]=>
  NULL
  ["Dept1"]=>
  NULL
  ["Dept2"]=>
  NULL
  ["College_Name"]=>
  string(9) "IIT Delhi"
}

```

**引用：**[https://www.php.net/manual/en/reflectionclass.getdefaultproperties.php](https://www.php.net/manual/en/reflectionclass.getdefaultproperties.php)