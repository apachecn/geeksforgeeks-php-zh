# PHP|ReflectionProperty getName()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionproperty-getname-function/](https://www.geeksforgeeks.org/php-reflectionproperty-getname-function/)

**ReflectionProperty：：getName()函数**是 PHP 中的内置函数，用于返回指定属性的名称。

**语法：**

```
*string* ReflectionProperty::getName ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定属性的名称。

以下程序说明 PHP：
**程序 1：**中的**ReflectionProperty：：getName()函数**

```
<?php

// Initializing a user-defined class Company
class Company
{
    public $SizeOfGeeksforGeeks = 13;
    protected $SizeOfGFG = 3;
}

// Using ReflectionProperty 
$A = new ReflectionProperty('Company', 'SizeOfGeeksforGeeks');
$B = new ReflectionProperty('Company', 'SizeOfGFG');

// Calling the getName() function
$C = $A->getName();
$D = $B->getName();

// Getting the name of the specified property.
var_dump($C);
var_dump($D);
?>
```

发帖主题：Re：Колибри0.7.0

```
string(19) "SizeOfGeeksforGeeks"
string(9) "SizeOfGFG"

```

**程序 2：**

```
<?php

// Initializing some user-defined classes
class Department1
{
    protected $SizeOfHR = 2;
}
class Department2
{
    public $SizeOfCoding = 6;
}
class Department3
{
    private $SizeOfMarketing = 9;
}

// Using ReflectionProperty over above classes
$A = new ReflectionProperty('Department1', 'SizeOfHR');
$B = new ReflectionProperty('Department2', 'SizeOfCoding');
$C = new ReflectionProperty('Department3', 'SizeOfMarketing');

// Calling the getName() function and
// getting the name of the specified property.
var_dump($A->getName());
var_dump($B->getName());
var_dump($C->getName());
?>
```

发帖主题：Re：Колибри0.7.0

```
string(8) "SizeOfHR"
string(12) "SizeOfCoding"
string(15) "SizeOfMarketing"

```

**引用：**[https://www.php.net/manual/en/reflectionproperty.getname.php](https://www.php.net/manual/en/reflectionproperty.getname.php)