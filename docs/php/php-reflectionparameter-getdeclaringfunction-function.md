# PHP|ReflectionParameter getDeclaringFunction()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionparameter-getdeclaringfunction-function/](https://www.geeksforgeeks.org/php-reflectionparameter-getdeclaringfunction-function/)

**ReflectionParameter：：getDeclaringFunction()函数**是 PHP 中的内置函数，用于返回声明函数。

**语法：**

```php
*ReflectionFunctionAbstract* ReflectionParameter::getDeclaringFunction ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回声明函数。

以下程序说明 PHP：
**程序 1：**中的**ReflectionParameter：：getDeclaringFunction()**函数

```php
<?php

// Initializing a user-defined class Company1
class Company1
{
    public function GFG($Parameter){}
}

// Initializing a subclass Company2
class Company2 extends Company1
{
}

// Using the ReflectionParameter over the above class
$A = new ReflectionParameter(['Company2', 'GFG'], 0); 

// Calling the getDeclaringFunction() function
$B = $A->getDeclaringFunction();

// Getting the specified declaring function
var_dump($B);
?>
```

发帖主题：Re：Колибри0.7.0

```php
object(ReflectionMethod)#2 (2) {
  ["name"]=>
  string(3) "GFG"
  ["class"]=>
  string(8) "Company1"
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
    public function Coding($Parameter2, $Parameter3){}
}
class Department3
{
    public function Marketing($Parameter4, $Parameter5, $Parameter6){}
}

// Using the ReflectionParameter over the above classes
$A = new ReflectionParameter(['Department1', 'HR'], 0);
$B = new ReflectionParameter(['Department2', 'Coding'], 1);
$C = new ReflectionParameter(['Department3', 'Marketing'], 2);

// Calling the getDeclaringFunction() function and
// getting the specified declaring functions
var_dump($A->getDeclaringFunction());
var_dump($B->getDeclaringFunction());
var_dump($C->getDeclaringFunction());
?>
```

发帖主题：Re：Колибри0.7.0

```php
object(ReflectionMethod)#4 (2) {
  ["name"]=>
  string(2) "HR"
  ["class"]=>
  string(11) "Department1"
}
object(ReflectionMethod)#4 (2) {
  ["name"]=>
  string(6) "Coding"
  ["class"]=>
  string(11) "Department2"
}
object(ReflectionMethod)#4 (2) {
  ["name"]=>
  string(9) "Marketing"
  ["class"]=>
  string(11) "Department3"
}

```

**引用：**[https://www.php.net/manual/en/reflectionparameter.getdeclaringfunction.php](https://www.php.net/manual/en/reflectionparameter.getdeclaringfunction.php)