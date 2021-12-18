# PHP|ReflectionClass getConstructor()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-getconstructor-function/](https://www.geeksforgeeks.org/php-reflectionclass-getconstructor-function/)

**ReflectionClass：：getConstructor()函数**是 PHP 中的一个内置函数，用于返回指定类的构造函数，如果该类没有任何构造函数，则返回 NULL。

**语法：**

```php
*ReflectionMethod* ReflectionClass::getConstructor( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定类的构造函数，如果该类没有任何构造函数，则返回 NULL。

下面的程序演示了 PHP 中的 ReflectionClass：：getConstructor()函数：

**程序 1：**

```php
<?php

// Using ReflectionClass over the class named as ReflectionClass
$Class = new ReflectionClass('ReflectionClass');

// Calling the getConstructor() function 
$constructor = $Class->getConstructor();

// Getting the constructor for the defined Class
var_dump($constructor);
?>
```

**输出：**

```php
object(ReflectionMethod)#2 (2) {
  ["name"]=>
  string(11) "__construct"
  ["class"]=>
  string(15) "ReflectionClass"
}

```

**程序 2：**

```php

// Defining a user-defined class Company
class Company {
    public function GeeksforGeeks() { }
    static function gfg() { }
}

// Using ReflectionClass over the class Company
$A = new ReflectionClass("Company");

// Calling the getConstructor() function
$B = $A->getConstructor();

// Getting the constructor for the defined Class
// or NULL if the constructor is not present
var_dump($B);
?>
```

**输出：**

```php
NULL

```

**引用：**[https://www.php.net/manual/en/reflectionclass.getconstructor.php](https://www.php.net/manual/en/reflectionclass.getconstructor.php)