# PHP|ReflectionParameter isVariadi()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionparameter-isvariadic-function/](https://www.geeksforgeeks.org/php-reflectionparameter-isvariadic-function/)

**ReflectionParameter：：isVariadi()函数**是 PHP 中的一个内置函数，用于在指定参数是可变参数时返回 true，否则返回 false。

**语法：**

```php
*bool* ReflectionParameter::isVariadic ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果指定的参数是可变参数，则此函数返回 TRUE，否则返回 FALSE。

下面的程序说明 PHP：
**程序 1：**中的**ReflectionParameter：：isVariadi()函数**

```php
<?php

// Initializing a user-defined class Company1
class Company1
{
    public function GFG( ...$Parameter){}
}

// Initializing a subclass Company2
class Company2 extends Company1
{
}

// Using the ReflectionParameter over the above class
$A = new ReflectionParameter(['Company2', 'GFG'], 0); 

// Calling the isVariadic() function
$B = $A->isVariadic();

// Getting TRUE if the specified parameter 
// is variadic, otherwise FALSE.
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
    function Coding( $Parameter2, $Par3 = 'Parameter_3'){}
}
class Department3
{
    function Marketing( &$Parameter4, ...$Parameter5){}
}

// Using the ReflectionParameter over the above classes
$A = new ReflectionParameter(['Department1', 'HR'], 0);
$B = new ReflectionParameter(['Department2', 'Coding'], 1);
$C = new ReflectionParameter(['Department3', 'Marketing'], 1);

// Calling the isVariadic() function and 
// getting TRUE if the specified parameter
// is variadic, otherwise FALSE.
var_dump($A->isVariadic());
var_dump($B->isVariadic());
var_dump($C->isVariadic());
?>
```

发帖主题：Re：Колибри0.7.0

```php
bool(false)
bool(false)
bool(true)

```

**引用：**[https://www.php.net/manual/en/reflectionparameter.isvariadic.php](https://www.php.net/manual/en/reflectionparameter.isvariadic.php)