# PHP|ReflectionProperty getDeclaringClass()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionproperty-getdeclaringclass-function/](https://www.geeksforgeeks.org/php-reflectionproperty-getdeclaringclass-function/)

**ReflectionProperty：：getDeclaringClass()函数**是 PHP 中的内置函数，用于返回指定的声明类。

**语法：**

```
*ReflectionClass* ReflectionProperty::getDeclaringClass ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定的声明类。

以下程序说明 PHP：
**程序 1：**中的**ReflectionProperty：：getDeclaringClass()函数**

```
<?php

// Initializing a user-defined class Company
class Company {
    public $SizeOfGeeksforGeeks = 13;
    public $SizeOfGFG = 3;
}

// Using ReflectionProperty 
$A = new ReflectionProperty('Company', 'SizeOfGeeksforGeeks');
$B = new ReflectionProperty('Company', 'SizeOfGFG');

// Calling the getDeclaringClass() function
$C = $A->getDeclaringClass();
$D = $B->getDeclaringClass();

// Getting the specified declaring classes
var_dump($C);
var_dump($D);
?>
```

发帖主题：Re：Колибри0.7.0

```
object(ReflectionClass)#3 (1) {
  ["name"]=>
  string(7) "Company"
}
object(ReflectionClass)#4 (1) {
  ["name"]=>
  string(7) "Company"
}

```

**程序 2：**

```
<?php

// Initializing some user-defined classes
class Department1
{
    public $SizeOfHR = 2;
}
class Department2
{
    public $SizeOfCoding = 6;
}
class Department3
{
    public $SizeOfMarketing = 9;
}

// Using ReflectionProperty over above classes
$A = new ReflectionProperty('Department1', 'SizeOfHR');
$B = new ReflectionProperty('Department2', 'SizeOfCoding');
$C = new ReflectionProperty('Department3', 'SizeOfMarketing');

// Calling the getDeclaringClass() function
$D = $A->getDeclaringClass();
$E = $B->getDeclaringClass();
$F = $C->getDeclaringClass();

// Getting the specified declaring classes
var_dump($D);
var_dump($E);
var_dump($F);
?>
```

发帖主题：Re：Колибри0.7.0

```
object(ReflectionClass)#4 (1) {
  ["name"]=>
  string(11) "Department1"
}
object(ReflectionClass)#5 (1) {
  ["name"]=>
  string(11) "Department2"
}
object(ReflectionClass)#6 (1) {
  ["name"]=>
  string(11) "Department3"
}

```

**引用：**[https://www.php.net/manual/en/reflectionproperty.getdeclaringclass.php](https://www.php.net/manual/en/reflectionproperty.getdeclaringclass.php)