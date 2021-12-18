# PHP|ReflectionParameter getclass()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionparameter-getclass-function/](https://www.geeksforgeeks.org/php-reflectionparameter-getclass-function/)

**ReflectionParameter：：getclass()函数**是 PHP 中的一个内置函数，用于返回参数提示的类类型。

**语法：**

```php
*ReflectionClass* ReflectionParameter::getClass ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回参数提示的类类型。

以下程序说明 PHP：
**程序 1：**中的**ReflectionParameter：：getclass()函数**

```php
<?php

// Initializing a user-defined class Company1
class Company1
{
    public function GFG( Exception $Parameter){}
}

// Initializing a subclass Company2
class Company2 extends Company1
{
}

// Using the ReflectionParameter over the above class
$A = new ReflectionParameter(['Company2', 'GFG'], 0); 

// Calling the getClass() function
$B = $A->getClass();

// Getting the class type hinted for the parameter.
var_dump($B);
?>
```

发帖主题：Re：Колибри0.7.0

```php
object(ReflectionClass)#2 (1) {
  ["name"]=>
  string(9) "Exception"
}

```

**程序 2：**

```php
<?php

// Initializing some user-defined classes
class Department1
{
    public function HR($Parameter1){}
}
class Department2
{
    public function Coding( Exception $Parameter2, Exception $Parameter3){}
}
class Department3
{
    public function Marketing($Parameter4, $Parameter5, $Parameter6){}
}

// Using the ReflectionParameter over the above classes
$A = new ReflectionParameter(['Department1', 'HR'], 0);
$B = new ReflectionParameter(['Department2', 'Coding'], 1);
$C = new ReflectionParameter(['Department3', 'Marketing'], 2);

// Calling the getClass() function and
// getting the class type hinted for the parameter.
var_dump($A->getClass());
var_dump($B->getClass());
var_dump($C->getClass());
?>
```

发帖主题：Re：Колибри0.7.0

```php
NULL
object(ReflectionClass)#4 (1) {
  ["name"]=>
  string(9) "Exception"
}
NULL

```

**引用：**[https://www.php.net/manual/en/reflectionparameter.getclass.php](https://www.php.net/manual/en/reflectionparameter.getclass.php)