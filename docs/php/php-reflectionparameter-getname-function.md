# PHP|ReflectionParameter getName()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionparameter-getname-function/](https://www.geeksforgeeks.org/php-reflectionparameter-getname-function/)

**ReflectionParameter：：getName()函数**是 PHP 中的内置函数，用于返回指定参数的名称。

**语法：**

```
 *string* ReflectionParameter::getName ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定参数的名称。

以下程序说明 PHP：
**程序 1：**中的**ReflectionParameter：：getName(**)函数

```
<?php

// Initializing a user-defined class Company1
class Company1
{
    public function GFG( $Parameter){}
}

// Initializing a subclass Company2
class Company2 extends Company1
{
}

// Using the ReflectionParameter over the above class
$A = new ReflectionParameter(['Company2', 'GFG'], 0); 

// Calling the getName() function
$B = $A->getName();

// Getting the name of the specified parameter.
var_dump($B);
?>
```

发帖主题：Re：Колибри0.7.0

```
string(9) "Parameter"

```

**程序 2：**

```
<?php

// Initializing some user-defined classes
class Department1
{
    protected function HR($Parameter1){}
}
class Department2
{
    final function Coding( Exception $Parameter2, Exception $Parameter3){}
}
class Department3
{
    function Marketing($Parameter4, $Parameter5, $Parameter6){}
}

// Using the ReflectionParameter over the above classes
$A = new ReflectionParameter(['Department1', 'HR'], 0);
$B = new ReflectionParameter(['Department2', 'Coding'], 1);
$C = new ReflectionParameter(['Department3', 'Marketing'], 2);

// Calling the getName() function and 
// getting the name of the specified parameter.
var_dump($A->getName());
var_dump($B->getName());
var_dump($C->getName());
?>
```

发帖主题：Re：Колибри0.7.0

```
string(10) "Parameter1"
string(10) "Parameter3"
string(10) "Parameter6"

```

**引用：**[https://www.php.net/manual/en/reflectionparameter.getname.php](https://www.php.net/manual/en/reflectionparameter.getname.php)