# PHP|反射 getName()函数

> Original: [https://www.geeksforgeeks.org/php-reflection-getname-function/](https://www.geeksforgeeks.org/php-reflection-getname-function/)

**Reflation：：getName()函数**是 PHP 中的内置函数，用于返回指定类的名称。

**语法：**

```
*string* Reflection::getName( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定类的名称。

下面的程序说明了 PHP 中的反射：：getName()函数：

**程序 1：**

```
<?php

// Defining a user-defined class named as Departments
class Departments {
    public $Dept1 = 'CSE';
    private $Dept2 = 'ECE';
    public static $Dept3 = 'EE';
}

// Using ReflectionClass over the class Departments
$ReflectionClass = new ReflectionClass('Departments');

// Calling getName() function 
$A = $ReflectionClass->getName();

// Getting the name of the specified class
var_dump($A);
?>
```

**输出：**

```
string(11) "Departments"

```

**程序 2：**

```
<?php

// Using ReflectionClass over the inbuilt class 'ReflectionClass'
$ReflectionClass = new ReflectionClass('ReflectionClass');

// Calling getName() function 
$A = $ReflectionClass->getName();

// Getting the name of the class
var_dump($A);
?>
```

**输出：**

```
string(15) "ReflectionClass"

```

**引用：**[https://www.php.net/manual/en/reflectionclass.getname.php](https://www.php.net/manual/en/reflectionclass.getname.php)