# PHP|ReflectionParameter isCallable()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionparameter-iscallable-function/](https://www.geeksforgeeks.org/php-reflectionparameter-iscallable-function/)

**ReflectionParameter：：isCallable()函数**是 PHP 中的一个内置函数，用于在指定参数可调用时返回 true，否则返回 false。

**语法：**

```php
*bool* ReflectionParameter::isCallable ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果指定的参数可调用，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明 PHP：
**程序 1：**中的**ReflectionParameter：：isCallable()函数**

```php
<?php

// Initializing a user-defined class Company1
class Company1
{
    public function GFG( callable $Parameter){}
}

// Initializing a subclass Company2
class Company2 extends Company1
{
}

// Using the ReflectionParameter over the above class
$A = new ReflectionParameter(['Company2', 'GFG'], 0); 

// Calling the isCallable() function
$B = $A->isCallable();

// Getting TRUE if the specified parameter
// is callable, FALSE otherwise.
var_dump($B);
?>
```

发帖主题：Re：Колибри0.7.0

```php
bool(true)

```

**程序 2：**

```php
<?php

// Initializing some user-defined classes
class Department1
{
    protected function HR( callable $Parameter1){}
}
class Department2
{
    final function Coding( $Parameter2, $Parameter3){}
}
class Department3
{
    function Marketing( sting $Parameter4, 
       string $Parameter5, string $Parameter6){}
}

// Using the ReflectionParameter over the above classes
$A = new ReflectionParameter(['Department1', 'HR'], 0);
$B = new ReflectionParameter(['Department2', 'Coding'], 1);
$C = new ReflectionParameter(['Department3', 'Marketing'], 2);

// Calling the isCallable() function and 
// getting TRUE if the specified parameter 
// is callable, FALSE otherwise.
var_dump($A->isCallable());
var_dump($B->isCallable());
var_dump($C->isCallable());
?>
```

发帖主题：Re：Колибри0.7.0

```php
bool(true)
bool(false)
bool(false)

```

**引用：**[https://www.php.net/manual/en/reflectionparameter.iscallable.php](https://www.php.net/manual/en/reflectionparameter.iscallable.php)