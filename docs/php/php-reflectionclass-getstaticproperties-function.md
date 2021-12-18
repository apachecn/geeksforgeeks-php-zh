# PHP|ReflectionClass getStaticProperties()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-getstaticproperties-function/](https://www.geeksforgeeks.org/php-reflectionclass-getstaticproperties-function/)

**ReflectionClass：：getStaticProperties()函数**是 PHP 中的内置函数，用于返回静态属性数组。 此函数目前没有文档，但有其参数列表。

**语法：**

```
ReflectionClass::getStaticProperties(void) : array
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回静态属性的数组。

以下程序说明 PHP：
**程序 1：**中的 ReflectionClass：：getStaticProperties()函数

```
<?php

// Defining a class named as Departments
class Departments {
    public $Dept1 = 'CSE';
    private $Dept2 = 'ECE';
    public static $Dept3 = 'EE';
}

// Using ReflectionClass over the class Departments
$ReflectionClass = new ReflectionClass('Departments');

// Calling getStaticProperties() function
$A = $ReflectionClass->getStaticProperties();

// Getting an array of the static properties
var_dump($A);
?>
```

发帖主题：Re：Колибри0.7.0

```
array(1) {
  ["Dept3"]=>
  string(2) "EE"
}

```

**程序 2：**

```
<?php

// Defining a class named as Departments
class GFG {
    static $name = "GeeksforGeeks";
    private static $addr = "Noida";
    protected static $email = 'abc@geeksforgeeks.org';
}

// Using ReflectionClass 
$ReflectionClass = new ReflectionClass('GFG');

// Calling getStaticProperties() function
$Property = $ReflectionClass->getStaticProperties();

// Getting an array of the static properties
// if present
var_dump($Property);
?>
```

发帖主题：Re：Колибри0.7.0

```
array(3) {
  ["name"]=>
  string(13) "GeeksforGeeks"
  ["addr"]=>
  string(5) "Noida"
  ["email"]=>
  string(21) "abc@geeksforgeeks.org"
}

```

**引用：**[https://www.php.net/manual/en/reflectionclass.getstaticproperties.php](https://www.php.net/manual/en/reflectionclass.getstaticproperties.php)