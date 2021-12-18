# PHP|ReflectionClass hasConstant()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-hasconstant-function/](https://www.geeksforgeeks.org/php-reflectionclass-hasconstant-function/)

**ReflectionClass：：hasConstant()函数**是 PHP 中的内置函数，用于检查指定的常量是否存在。

**语法：**

```php
*bool* ReflectionClass::hasConstant( *string* $name )
```

**参数：**此函数接受单个参数**$name**，该参数保存已定义常量的名称。

**返回值：**如果定义了常量，则此函数返回 TRUE，否则返回 FALSE。

下面的程序演示了 PHP 中的 ReflectionClass：：hasConstant()函数：

**程序 1：**

```php
<?php

// Defining a user-defined class Company
class Company {
    const c1 = 'GeeksforGeeks';
}

// Using the ReflectionClass over the
// defined user-defined class Company
$constant = new ReflectionClass("Company");

// Calling the hasConstant() function
$const = $constant->hasConstant("c1");

// Getting the value TRUE or FALSE
var_dump($const);
?>
```

**输出：**

```php
bool(true)

```

**程序 2：**

```php
<?php

// Defining an empty class
class Company {
}

// Using the ReflectionClass over the
// defined user-defined class Company
$constant = new ReflectionClass("Company");

// Calling the hasConstant() function and
// getting the value TRUE or FALSE
var_dump($constant->hasConstant("c1"));
?>
```

**输出：**

```php
bool(false)

```

**引用：**[https://secure.php.net/manual/en/reflectionclass.hasconstant.php](https://secure.php.net/manual/en/reflectionclass.hasconstant.php)