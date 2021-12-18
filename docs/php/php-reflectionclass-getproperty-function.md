# PHP|ReflectionClass getProperty()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-getproperty-function/](https://www.geeksforgeeks.org/php-reflectionclass-getproperty-function/)

**ReflectionClass：：getProperty()函数**是 PHP 中的内置函数，用于返回指定类的 ReflectionProperty 数组。

**语法：**

```
ReflectionClass::getProperty ( string $name ) : array
```

**参数：**此函数接受参数**name**，它是属性的名称。

**返回值：**此函数返回指定类的 ReflectionProperty 数组。

以下程序说明 PHP：
**程序 1：**中的 ReflectionClass：：getProperty()函数

```
<?php

// Using ReflectionClass 
$ReflectionClass = new ReflectionClass('ReflectionClass');

// Initialising a property name
$a = 'name';

// Calling getProperty() function over 
// the property name
$Property = $ReflectionClass->getProperty($a);

// Getting an array of the ReflectionProperty
// for the specified class.
var_dump($Property);
?>
```

发帖主题：Re：Колибри0.7.0

```
object(ReflectionProperty)#2 (2) {
  ["name"]=>
  string(4) "name"
  ["class"]=>
  string(15) "ReflectionClass"
}

```

**程序 2：**

```
<?php

// Defining a class named as Company
class Company {
    public $C1;
    private $C2;
    public static $C3;
}

// Using ReflectionClass over the class Company
$ReflectionClass = new ReflectionClass('Company');

// Calling getPropertY() function 
$A = $ReflectionClass->getProperty('C1');

// Getting an array of the reflected property
var_dump($A);
?>
```

**Output:**

```
object(ReflectionProperty)#2 (2) {
  ["name"]=>
  string(2) "C1"
  ["class"]=>
  string(7) "Company"
}

```

**引用：**[https://www.php.net/manual/en/reflectionclass.getproperties.php](https://www.php.net/manual/en/reflectionclass.getproperties.php)