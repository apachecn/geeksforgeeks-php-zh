# PHP|ReflectionParameter getDefaultValue()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionparameter-getdefaultvalue-function/](https://www.geeksforgeeks.org/php-reflectionparameter-getdefaultvalue-function/)

**ReflectionParameter：：getDefaultValue()函数**是 PHP 中的内置函数，用于为指定的用户定义函数或方法返回参数的默认值。

**语法：**

```php
 *mixed* ReflectionParameter::getDefaultValue ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定用户定义函数或方法的参数的默认值。

以下程序说明 PHP：
**程序 1：**中的**ReflectionParameter：：getDefaultValue()函数**

```php
<?php

// Initializing a user-defined class Company1
class Company1
{
    function GFG($Full_Name = 'GeeksforGeeks'){}
}

// Initializing a subclass Company2
class Company2 extends Company1
{
}

// Using the ReflectionParameter over the above class
$A = new ReflectionParameter(['Company2', 'GFG'], 0); 

// Calling the getDefaultValue() function
$B = $A->getDefaultValue();

// Getting the default value of the parameter
var_dump($B);
?>
```

发帖主题：Re：Колибри0.7.0

```php
string(13) "GeeksforGeeks"

```

**程序 2：**

```php
<?php

// Initializing some user-defined classes
class Department1
{
    function HR( $Full_Name = 'Human Resource'){}
}
class Department2
{
    function Coding( $Parameter2, $Par3 = 'Parameter3'){}
}
class Department3
{
    function Marketing( $Parameter4 = 'Digital Marketing', $Parameter5){}
}

// Using the ReflectionParameter over the above classes
$A = new ReflectionParameter(['Department1', 'HR'], 0);
$B = new ReflectionParameter(['Department2', 'Coding'], 1);
$C = new ReflectionParameter(['Department3', 'Marketing'], 0);

// Calling the getDefaultValue() function and 
// getting the default value of the parameter
var_dump($A->getDefaultValue());
var_dump($B->getDefaultValue());
var_dump($C->getDefaultValue());
?>
```

发帖主题：Re：Колибри0.7.0

```php
string(14) "Human Resource"
string(10) "Parameter3"
string(17) "Digital Marketing"

```

**引用：**[https://www.php.net/manual/en/reflectionparameter.getdefaultvalue.php](https://www.php.net/manual/en/reflectionparameter.getdefaultvalue.php)