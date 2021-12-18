# PHP|ReflectionClass isAbstract()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-isabstract-function/](https://www.geeksforgeeks.org/php-reflectionclass-isabstract-function/)

**ReflectionClass：：isAbstract()函数**是 PHP 中的内置函数，用于检查指定类是否抽象。

**语法：**

```php
*bool* ReflectionClass::isAbstract( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的程序演示了 PHP 中的 ReflectionClass：：isAbstract()函数：

**程序 1：**

```php
<?php

// Defining a abstract class abstractGFG
abstract class abstractGFG {}

// Using ReflectionClass over the above 
// abstractGFG class
$Class = new ReflectionClass('abstractGFG');

// Calling isAbstract() function
$A = $Class->isAbstract();

// Getting the value either true or false
var_dump($A);
?>
```

**输出：**

```php
bool(true)

```

**程序 2：**

```php
<?php

// Defining a user-defined class Company
class Company {
    Public Function GeeksforGeeks() {}
    Private Function GFG() {}
}

// Using ReflectionClass over the above 
// Company class
$Class = new ReflectionClass('Company');

// Calling isAbstract() function
$A = $Class->isAbstract();

// Getting the value either true or false
var_dump($A);
?>
```

**输出：**

```php
bool(false)

```

**引用：**[https://www.php.net/manual/en/reflectionclass.isabstract.php](https://www.php.net/manual/en/reflectionclass.isabstract.php)