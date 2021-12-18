# PHP|ReflectionProperty isPrivate()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionproperty-isprivate-function/](https://www.geeksforgeeks.org/php-reflectionproperty-isprivate-function/)

**ReflectionProperty：：isPrivate()函数**是 PHP 中的一个内置函数，用于在指定属性为私有时返回 true，否则返回 false。

**语法：**

```php
*bool* ReflectionProperty::isPrivate ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果指定的属性是私有的，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明 PHP：
**程序 1：**中的**ReflectionProperty：：isPrivate()函数**

```php
<?php

// Initializing a user-defined class Company
class Company
{
    private $SizeOfGeeksforGeeks = 13;
    public $SizeOfGFG = 3;
}

// Using ReflectionProperty 
$A = new ReflectionProperty('Company', 'SizeOfGeeksforGeeks');
$B = new ReflectionProperty('Company', 'SizeOfGFG');

// Calling the isPrivate() function
$C = $A->isPrivate();
$D = $B->isPrivate();

// Getting TRUE if the specified property
// is private, FALSE otherwise.
var_dump($C);
var_dump($D);
?>
```

发帖主题：Re：Колибри0.7.0

```php
bool(true)
bool(false)

```

**程序 2：**

```php
<?php

// Initializing some user-defined classes
class Department1
{
    protected $SizeOfHR;
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

// Calling the isPrivate() function and
// getting TRUE if the specified property
// is private, FALSE otherwise.
var_dump($A->isPrivate());
var_dump($B->isPrivate());
var_dump($C->isPrivate());
?>
```

发帖主题：Re：Колибри0.7.0

```php
bool(false)
bool(false)
bool(true)

```

**引用：**[https://www.php.net/manual/en/reflectionproperty.isprivate.php](https://www.php.net/manual/en/reflectionproperty.isprivate.php)