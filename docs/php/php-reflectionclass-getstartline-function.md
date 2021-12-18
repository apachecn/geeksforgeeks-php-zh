# PHP|ReflectionClass getStartLine()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-getstartline-function/](https://www.geeksforgeeks.org/php-reflectionclass-getstartline-function/)

**ReflectionClass：：getStartLine()函数**是 PHP 中的一个内置函数，用于返回用户定义的类开始时的行号。

**语法：**

```
*int* ReflectionClass::getStartLine( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回用户定义类开始的行号。

下面的程序演示了 PHP 中的 ReflectionClass：：getStartLine()函数：

**程序 1：**

```
<?php

// Defining a class named as Departments
class Departments {}

// Using ReflectionClass over the class Departments
$ReflectionClass = new ReflectionClass('Departments');

// Calling getStartLine() functions
$A = $ReflectionClass->getStartLine();

// Getting the start line number of 
// the specified class
var_dump($A);
?>
```

**输出：**

```
int(4)

```

**程序 2：**

```
<?php

// Defining a class named as Departments
class Departments {
    static $Dept1 = 'CSE';
    private static $Dept2 = 'ECE';
    public static $Dept3 = 'EE';
}

// Using ReflectionClass over the class Departments
$ReflectionClass = new ReflectionClass('Departments');

// Calling getStartLine() functions
$A = $ReflectionClass->getStartLine();

// Getting the start line number of 
// the specified class
var_dump($A);
?>
```

**输出：**

```
int(4)

```

**引用：**[https://www.php.net/manual/en/reflectionclass.getstartline.php](https://www.php.net/manual/en/reflectionclass.getstartline.php)