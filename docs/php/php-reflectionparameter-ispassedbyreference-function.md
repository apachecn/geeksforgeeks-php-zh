# PHP|ReflectionParameter isPassedByReference()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionparameter-ispassedbyreference-function/](https://www.geeksforgeeks.org/php-reflectionparameter-ispassedbyreference-function/)

**ReflectionParameter：：isPassedByReference()函数**是 PHP 中的一个内置函数，用于在通过引用传递指定参数时返回 true，否则返回 false。

**语法：**

```php
 *bool* ReflectionParameter::isPassedByReference ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果指定的参数是通过引用传递的，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明 PHP：
**程序 1：**中的**ReflectionParameter：：isPassedByReference()函数**

```php
<?php

// Initializing a user-defined class Company1
class Company1
{
    public function GFG(array &$Parameter){}
}

// Initializing a subclass Company2
class Company2 extends Company1
{
}

// Using the ReflectionParameter over the above class
$A = new ReflectionParameter(['Company2', 'GFG'], 0); 

// Calling the isPassedByReference() function
$B = $A->isPassedByReference();

// Getting TRUE if the specified parameter 
// is passed by reference, otherwise FALSE.
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
    function HR( $Full_Name){}
}
class Department2
{
    function Coding( $Parameter2, $Par3 = 'Parameter3'){}
}
class Department3
{
    function Marketing( &$Parameter4, $Parameter5){}
}

// Using the ReflectionParameter over the above classes
$A = new ReflectionParameter(['Department1', 'HR'], 0);
$B = new ReflectionParameter(['Department2', 'Coding'], 1);
$C = new ReflectionParameter(['Department3', 'Marketing'], 0);

// Calling the isPassedByReference() function and 
// getting TRUE if the specified parameter
// is passed by reference, otherwise FALSE.
var_dump($A->isPassedByReference());
var_dump($B->isPassedByReference());
var_dump($C->isPassedByReference());
?>
```

发帖主题：Re：Колибри0.7.0

```php
bool(false)
bool(false)
bool(true)

```

**引用：**[https://www.php.net/manual/en/reflectionparameter.ispassedbyreference.php](https://www.php.net/manual/en/reflectionparameter.ispassedbyreference.php)