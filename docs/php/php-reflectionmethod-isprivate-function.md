# PHP|ReflectionMethod isPrivate()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionmethod-isprivate-function/](https://www.geeksforgeeks.org/php-reflectionmethod-isprivate-function/)

**ReflectionMethod：：isPrivate()函数**是 PHP 中的一个内置函数，用于在指定的方法是私有的时返回 TRUE，否则返回 FALSE。

**语法：**

```php
*bool* ReflectionMethod::isPrivate( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果指定的方法是私有的，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明了 PHP 中的 ReflectionMethod：：isPrivate()函数：

**程序 1：**

```php
<?php

// Initializing a user-defined class
class Company {

    private function GFG() {}
}

// Using ReflectionMethod() over the class Company
$A = new ReflectionMethod('Company', 'GFG');

// Calling the isPrivate() function
$B = $A->isPrivate();

// Getting the value TRUE if the specified
// method is private, otherwise FALSE.
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

    private function Coding() {}
}

class Department3 {

     function marketing(){}
}

// Using ReflectionMethod() over the above classes
$A = new ReflectionMethod('Department1', 'hR');
$B = new ReflectionMethod('Department2', 'Coding');
$C = new ReflectionMethod('Department3', 'marketing');

// Calling the isPrivate() function and 
// getting the value TRUE if the specified
// method is private, otherwise FALSE.
var_dump($A->isPrivate());
var_dump($B->isPrivate());
var_dump($C->isPrivate());
?>
```

**输出：**

```php
bool(false)
bool(true)
bool(false)

```

**引用：**[https://www.php.net/manual/en/reflectionmethod.isprivate.php](https://www.php.net/manual/en/reflectionmethod.isprivate.php)