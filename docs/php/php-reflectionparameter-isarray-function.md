# PHP|ReflectionParameter isArray()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionparameter-isarray-function/](https://www.geeksforgeeks.org/php-reflectionparameter-isarray-function/)

**ReflectionParameter：：isArray()函数**是 PHP 中的内置函数，用于在指定参数为数组时返回 TRUE，否则返回 FALSE。

**语法：**

```php
 *bool* ReflectionParameter::isArray ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果指定的参数是数组，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明 PHP：
**程序 1：**中的**ReflectionParameter：：isArray()函数**

```php
<?php

// Initializing a user-defined class Company1
class Company1
{
    public function GFG( array $Parameter){}
}

// Initializing a subclass Company2
class Company2 extends Company1
{
}

// Using the ReflectionParameter over the above class
$A = new ReflectionParameter(['Company2', 'GFG'], 0); 

// Calling the isArray() function
$B = $A->isArray();

// Getting TRUE if the specified parameter
// is an array, FALSE otherwise.
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
    protected function HR(array $Parameter1){}
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

// Calling the isArray() function and 
// getting TRUE if the specified parameter 
// is an array, FALSE otherwise.
var_dump($A->isArray());
var_dump($B->isArray());
var_dump($C->isArray());
?>
```

发帖主题：Re：Колибри0.7.0

```php
bool(true)
bool(false)
bool(false)

```

**引用：**[https://www.php.net/manual/en/reflectionparameter.isarray.php](https://www.php.net/manual/en/reflectionparameter.isarray.php)