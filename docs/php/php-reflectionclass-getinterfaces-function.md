# PHP|ReflectionClass getInterfaces()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-getinterfaces-function/](https://www.geeksforgeeks.org/php-reflectionclass-getinterfaces-function/)

**ReflectionClass：：getInterfaces()函数**是 PHP 中的内置函数，用于返回接口的关联数组。 这些返回的数组包含作为接口名称的键和作为 ReflectionClass 对象的数组值。

**语法：**

```
*array* ReflectionClass::getInterfaces( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回接口的关联数组。 这些返回的数组包含作为接口名称的键和作为 ReflectionClass 对象的数组值。

下面的程序演示了 PHP 中的 ReflectionClass：：getInterfaces()函数：

**程序 1：**

```
<?php

// Defining some interfaces
interface Colleges { }
interface Departments { }
interface Students { }
interface Companies { }

// Initialising a class of Interfaces
class Interfaces implements Colleges, Departments, Students, Companies { }

// Using ReflectionClass over the class Interfaces
$A = new ReflectionClass("Interfaces");

// Calling the getInterfaces() function
$B = $A->getInterfaces();

// Getting the associative array of interfaces
print_r($B);
?>
```

**输出：**

```
Array
(
    [Colleges] => ReflectionClass Object
        (
            [name] => Colleges
        )

    [Departments] => ReflectionClass Object
        (
            [name] => Departments
        )

    [Students] => ReflectionClass Object
        (
            [name] => Students
        )

    [Companies] => ReflectionClass Object
        (
            [name] => Companies
        )

)

```

**程序 2：**

```
<?php

// Using ReflectionClass 
$ReflectionClass = new ReflectionClass('ReflectionClass');

// Calling getInterfaces() functions
$A = $ReflectionClass->getInterfaces();

// Getting the associative array of interfaces
var_dump($A);
?>
```

**输出：**

```
array(1) {
  ["Reflector"]=>
  object(ReflectionClass)#2 (1) {
    ["name"]=>
    string(9) "Reflector"
  }
}

```

**引用：**[https://www.php.net/manual/en/reflectionclass.getinterfaces.php](https://www.php.net/manual/en/reflectionclass.getinterfaces.php)