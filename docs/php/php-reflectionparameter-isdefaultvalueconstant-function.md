# PHP|ReflectionParameter isDefaultValueConstant()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionparameter-isdefaultvalueconstant-function/](https://www.geeksforgeeks.org/php-reflectionparameter-isdefaultvalueconstant-function/)

**ReflectionParameter：：isDefaultValueConstant()函数**是 PHP 中的一个内置函数，用于在默认值为常量时返回 TRUE，否则返回 FALSE。

**语法：**

```php
*bool* ReflectionParameter::isDefaultValueConstant ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果默认值为常量，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明 PHP：
**程序 1：**中的**ReflectionParameter：：isDefaultValueConstant()函数**

```php
<?php

// Initializing a user-defined class Company1
class Company1
{
    function GFG($Full_Name = GeeksforGeeks){}
}

// Initializing a subclass Company2
class Company2 extends Company1
{
}

// Using the ReflectionParameter over the above class
$A = new ReflectionParameter(['Company2', 'GFG'], 0); 

// Calling the isDefaultValueConstant() function
$B = $A->isDefaultValueConstant();

// Getting TRUE if the default value is 
// constant, and FALSE otherwise.
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
    function HR( $Full_Name = Human_Resource){}
}
class Department2
{
    function Coding( $Parameter2, $Par3 = 'Parameter3'){}
}
class Department3
{
    function Marketing( $Parameter4, $Parameter5 = Digital_Marketing){}
}

// Using the ReflectionParameter over the above classes
$A = new ReflectionParameter(['Department1', 'HR'], 0);
$B = new ReflectionParameter(['Department2', 'Coding'], 1);
$C = new ReflectionParameter(['Department3', 'Marketing'], 1);

// Calling the isDefaultValueConstant() function and 
// getting TRUE if the default value is 
// constant, and FALSE otherwise.
var_dump($A->isDefaultValueConstant());
var_dump($B->isDefaultValueConstant());
var_dump($C->isDefaultValueConstant());
?>
```

发帖主题：Re：Колибри0.7.0

```php
bool(true)
bool(false)
bool(true)

```

**引用：**[https://www.php.net/manual/en/reflectionparameter.isdefaultvalueconstant.php](https://www.php.net/manual/en/reflectionparameter.isdefaultvalueconstant.php)