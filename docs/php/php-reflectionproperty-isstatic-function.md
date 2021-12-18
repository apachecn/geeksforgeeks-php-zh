# PHP|ReflectionProperty isStatic()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionproperty-isstatic-function/](https://www.geeksforgeeks.org/php-reflectionproperty-isstatic-function/)

**ReflectionProperty：：isStatic()函数**是 PHP 中的一个内置函数，用于在指定的属性为静态属性时返回 True，否则返回 False。

**语法：**

```
*bool* ReflectionProperty::isStatic( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果指定的属性是静态的，则此函数返回 TRUE，否则返回 FALSE。

下面的程序说明了 PHP 中的**ReflectionProperty：：isStatic()函数**：

**程序 1：**

```
<?php

// Initializing a user-defined class Company
class Company
{
    protected $SizeOfGeeksforGeeks = 13;
    static $SizeOfGFG = 3;
}

// Using ReflectionProperty 
$A = new ReflectionProperty('Company', 'SizeOfGeeksforGeeks');
$B = new ReflectionProperty('Company', 'SizeOfGFG');

// Calling the isStatic() function
$C = $A->isStatic();
$D = $B->isStatic();

// Getting TRUE if the specified property
// is static, FALSE otherwise.
var_dump($C);
var_dump($D);
?>
```

**输出：**

```
bool(false)
bool(true)

```

**程序 2：**

```
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
    static $SizeOfMarketing = 9;
}

// Using ReflectionProperty over above classes
$A = new ReflectionProperty('Department1', 'SizeOfHR');
$B = new ReflectionProperty('Department2', 'SizeOfCoding');
$C = new ReflectionProperty('Department3', 'SizeOfMarketing');

// Calling the isStatic() function and
// getting TRUE if the specified property
// is static, FALSE otherwise.
var_dump($A->isStatic());
var_dump($B->isStatic());
var_dump($C->isStatic());
?>
```

**输出：**

```
bool(false)
bool(false)
bool(true)

```

**引用：**[https://secure.php.net/manual/en/reflectionproperty.isstatic.php](https://secure.php.net/manual/en/reflectionproperty.isstatic.php)