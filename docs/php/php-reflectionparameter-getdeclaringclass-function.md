# PHP|ReflectionParameter getDeclaringClass()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionparameter-getdeclaringclass-function/](https://www.geeksforgeeks.org/php-reflectionparameter-getdeclaringclass-function/)

**ReflectionParameter：：getDeclaringClass()函数**是 PHP 中的内置函数，用于返回声明类。

**语法：**

```
*ReflectionClass* ReflectionParameter::getDeclaringClass ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回声明类。

以下程序说明 PHP：
**程序 1：**中的 ReflectionParameter：：getDeclaringClass()函数

```
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

// Calling the getDeclaringClass() function
$B = $A->getDeclaringClass();

// Getting the specified declaring class
var_dump($B);
?>
```

发帖主题：Re：Колибри0.7.0

```
object(ReflectionClass)#2 (1) {
  ["name"]=>
  string(8) "Company1"
}

```

**程序 2：**

```
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

// Calling the getDeclaringClass() function and
// getting the specified declaring classes
var_dump($A->getDeclaringClass());
var_dump($B->getDeclaringClass());
var_dump($C->getDeclaringClass());
?>
```

发帖主题：Re：Колибри0.7.0

```
object(ReflectionClass)#4 (1) {
  ["name"]=>
  string(11) "Department1"
}
object(ReflectionClass)#4 (1) {
  ["name"]=>
  string(11) "Department2"
}
object(ReflectionClass)#4 (1) {
  ["name"]=>
  string(11) "Department3"
}

```

**引用：**[https://www.php.net/manual/en/reflectionparameter.getdeclaringclass.php](https://www.php.net/manual/en/reflectionparameter.getdeclaringclass.php)