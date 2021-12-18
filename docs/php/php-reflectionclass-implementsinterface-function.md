# PHP|ReflectionClass implementsInterface()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-implementsinterface-function/](https://www.geeksforgeeks.org/php-reflectionclass-implementsinterface-function/)

**ReflectionClass：：ImplementsInterface()函数**是 PHP 中的内置函数，用于检查指定接口是否存在。

**语法：**

```php
*bool* ReflectionClass::implementsInterface( *string* $interface )
```

**参数：**此函数接受单个参数**$interface**，该参数保存正在检查的指定接口。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的程序演示了 PHP 中的 ReflectionClass：：ImplementsInterface()函数：

**程序 1：**

```php
<?php

// Defining some interfaces
interface Colleges { }
interface Departments { }
interface Students { }
interface Companies { }

// Initialising a class of Interfaces
class Interfaces implements Colleges, 
        Departments, Students, Companies { }

// Using ReflectionClass over the class Interfaces
$A = new ReflectionClass("Interfaces");

// Calling the implementsInterface() function
// over the Interface 'Colleges'
$B = $A->implementsInterface('Colleges');

// Getting the value true or false
var_dump($B);
?>
```

**输出：**

```php
bool(true)

```

**程序 2：**

```php
<?php

// Defining a SuperClass interface Company 
interface Company {
    public function GFG();
}

// Defining a different interface Company1
interface Company1 {
    public function GeeksforGeeks();
}

// Defining a subclass Departments
class Departments implements Company {
    public function GFG() {}
}

// Using ReflectionClass() over the 
// subclass Departments
$reflect = new ReflectionClass('Departments');

// Calling implementsInterface() function
$A = $reflect->implementsInterface('Company1');

// Getting the value either true or false
var_dump($A);

?>
```

**输出：**

```php
bool(false)

```

**引用：**[https://www.php.net/manual/en/reflectionclass.implementsinterface.php](https://www.php.net/manual/en/reflectionclass.implementsinterface.php)