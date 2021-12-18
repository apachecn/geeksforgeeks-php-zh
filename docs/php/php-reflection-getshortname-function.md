# PHP|反射 getShortName()函数

> Original: [https://www.geeksforgeeks.org/php-reflection-getshortname-function/](https://www.geeksforgeeks.org/php-reflection-getshortname-function/)

**Reflation：：getShortName()函数**是 PHP 中的一个内置函数，用于返回指定类的短名称，即没有命名空间的部分。

**语法：**

```php
*string* Reflection::getShortName( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定类的短名称，即没有命名空间的部分。

下面的程序说明了 PHP 中的反射：：getShortName()函数：

**程序 1：**

```php
<?php

// Defining a namespace and class GFG
namespace A\B;
class GFG{ } 

// Using ReflectionClass over the namespace and
// specified class GFG
$ReflectionClass = new \ReflectionClass('A\\B\\GFG');

// Calling getShortName() function 
$A = $ReflectionClass->getShortName();

// Getting the short name of the specified class
var_dump($A);
?>
```

**输出：**

```php
string(3) "GFG"

```

**程序 2：**

```php
<?php

// Using ReflectionClass inbuilt function
$ReflectionClass = new ReflectionClass('ReflectionClass');

// Calling getShortName() functions
$A = $ReflectionClass->getShortName();

// Getting the short name of the specified class
var_dump($A);
?>
```

**输出：**

```php
string(15) "ReflectionClass"

```

**引用：**[https://www.php.net/manual/en/reflectionclass.getshortname.php](https://www.php.net/manual/en/reflectionclass.getshortname.php)