# PHP|ReflectionMethod isConstructor()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionmethod-isconstructor-function/](https://www.geeksforgeeks.org/php-reflectionmethod-isconstructor-function/)

**ReflectionMethod：：isConstructor()函数**是 PHP 中的内置函数，用于在指定的方法是构造函数时返回 TRUE，否则返回 FALSE。

**语法：**

```php
*bool* ReflectionMethod::isConstructor( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果指定的方法是构造函数，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明了 PHP 中的 ReflectionMethod：：isConstructor()函数：

**程序 1：**

```php
<?php

// Initializing a user-defined class
class Company {

    function __construct() {}
}

// Using ReflectionMethod() over the class Company
$A = new ReflectionMethod('Company', '__construct');

// Calling the isConstructor() function
$B = $A->isConstructor();

// Getting the value TRUE if the specified
// method is constructor, otherwise FALSE.
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

// Initializing some user-defined classes
class Department1 {

    public function hr($name) {
        return 'HR' . $name;
    }
}
class Department2 {
    function __construct() {}
}

class Department3 {
     function marketing(){}
}

// Using ReflectionMethod() over the above classes
$A = new ReflectionMethod('Department1', 'hR');
$B = new ReflectionMethod('Department2', '__construct');
$C = new ReflectionMethod('Department3', 'marketing');

// Calling the isConstructor() function and 
// getting the value TRUE if the specified
// method is constructor, otherwise FALSE.
var_dump($A->isConstructor());
var_dump($B->isConstructor());
var_dump($C->isConstructor());
?>
```

**输出：**

```php
bool(false)
bool(true)
bool(false)

```

**引用：**[https://www.php.net/manual/en/reflectionmethod.isconstructor.php](https://www.php.net/manual/en/reflectionmethod.isconstructor.php)