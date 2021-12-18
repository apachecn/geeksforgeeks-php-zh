# PHP|ReflectionProperty getModifier()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionproperty-getmodifiers-function/](https://www.geeksforgeeks.org/php-reflectionproperty-getmodifiers-function/)

**ReflectionProperty：：getModifier()函数**是 PHP 中的内置函数，用于返回指定修饰符的数字表示形式。

**语法：**

```php
*int* ReflectionProperty::getModifiers ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定修饰符的数字表示形式。

下面的程序演示了 PHP 中的**ReflectionProperty：：getModifier()函数**：

**程序 1：**

```php
<?php

// Initializing a user-defined class Company
class Company {
    public $SizeOfGeeksforGeeks = 13;
    protected $SizeOfGFG = 3;
}

// Using ReflectionProperty 
$A = new ReflectionProperty('Company', 'SizeOfGeeksforGeeks');
$B = new ReflectionProperty('Company', 'SizeOfGFG');

// Calling the getModifiers() function
$C = $A->getModifiers();
$D = $B->getModifiers();

// Getting the numeric representation of
// the specified modifiers.
var_dump($C);
var_dump($D);
?>
```

**输出：**

```php
int(256)
int(512)

```

**程序 2：**

```php
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

// Calling the getModifiers() function
$D = $A->getModifiers();
$E = $B->getModifiers();
$F = $C->getModifiers();

// Getting the numeric representation
// of the specified modifiers.
var_dump($D);
var_dump($E);
var_dump($F);
?>
```

**输出：**

```php
int(512)
int(256)
int(1024)

```

**引用：**[https://www.php.net/manual/en/reflectionproperty.getmodifiers.php](https://www.php.net/manual/en/reflectionproperty.getmodifiers.php)