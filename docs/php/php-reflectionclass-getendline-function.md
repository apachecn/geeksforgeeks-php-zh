# PHP|ReflectionClass getEndLine()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-getendline-function/](https://www.geeksforgeeks.org/php-reflectionclass-getendline-function/)

**ReflectionClass：：getEndLine()函数**是 PHP 中的一个内置函数，用于返回用户定义的类 get 结束的行号。

**语法：**

```php
*int* ReflectionClass::getEndLine( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回用户定义的类 get 结束的行号。

下面的程序演示了 PHP 中的 ReflectionClass：：getEndLine()函数：

**程序 1：**

```php
<?php

// Defining a class named as Departments
class Departments {}

// Using ReflectionClass over the class Departments
$ReflectionClass = new ReflectionClass('Departments');

// Calling getEndLine() functions
$A = $ReflectionClass->getEndLine();

// Getting the end line number of 
// the specified class
var_dump($A);
?>
```

**输出：**

```php
int(4)

```

**程序 2：**

```php
<?php

// Defining a class named as Departments
class Departments {
    static $Dept1 = 'CSE';
    private static $Dept2 = 'ECE';
    public static $Dept3 = 'EE';
}

// Using ReflectionClass over the class Departments
$ReflectionClass = new ReflectionClass('Departments');

// Calling getEndLine() functions
$A = $ReflectionClass->getEndLine();

// Getting the end line number of 
// the specified class
var_dump($A);
?>
```

**输出：**

```php
int(8)

```

**引用：**[https://www.php.net/manual/en/reflectionclass.getendline.php](https://www.php.net/manual/en/reflectionclass.getendline.php)