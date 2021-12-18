# PHP|ReflectionClass getFileName()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-getfilename-function/](https://www.geeksforgeeks.org/php-reflectionclass-getfilename-function/)

**ReflectionClass：：getFileName()函数**是 PHP 中的一个内置函数，用于返回定义了类的文件的文件名，如果找不到该文件，则返回 False。

**语法：**

```
*string* ReflectionClass::getFileName( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回定义了类的文件的文件名，如果找不到该文件，则返回 False。

下面的程序演示了 PHP 中的 ReflectionClass：：getFileName()函数：

**程序 1：**

```
<?php

// Defining a user-defined class
// named as Departments
class Departments {
    static $Dept1 = 'CSE';
    private static $Dept2 = 'ECE';
    public static $Dept3 = 'EE';
}

// Using ReflectionClass over the class Departments
$ReflectionClass = new ReflectionClass('Departments');

// Calling getFileName() functions
$A = $ReflectionClass->getFileName();

// Getting the name of the file 
// in which the class has been defined
var_dump($A);
?>
```

**输出：**

```
string(23) "C:\xampp\htdocs\gfg.php"

```

**程序 2：**

```
<?php

// Using ReflectionClass 
$ReflectionClass = new ReflectionClass('ReflectionClass');

// Calling getFileName() functions
$A = $ReflectionClass->getFileName();

// Getting the name of the file 
// in which the class has been defined
var_dump($A);
?>
```

**输出：**

```
bool(false)

```

**引用：**[https://www.php.net/manual/en/reflectionclass.getfilename.php](https://www.php.net/manual/en/reflectionclass.getfilename.php)