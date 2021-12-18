# PHP|ReflectionClass isInstance()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-isinstance-function/](https://www.geeksforgeeks.org/php-reflectionclass-isinstance-function/)

**ReflectionClass：：isInstance()函数**是 PHP 中的一个内置函数，用于检查指定的对象是否为类的实例。

**语法：**

```php
*bool* ReflectionClass::isInstance( *object* $object )
```

**参数：**此函数接受在类的实例中搜索的单个参数**对象**。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的程序说明了 PHP 中的**ReflectionClass：：isInstance()函数**：

**程序 1：**

```php
<?php

// Declaring a user-defined class
class  GFG { }

// Initialising the instance
$Instance = new GFG();

// Using ReflectionClass over the
// instance GFG
$obj = new ReflectionClass('GFG');

// Calling isInstance() function
$A = $obj->isInstance($Instance);

// Getting the value true or false
var_dump($A);
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Declaring a user-defined class
class  GFG { }

// Using ReflectionClass over the
// instance GFG
$obj = new ReflectionClass('GFG');

// Calling isInstance() function
$A = $obj->isInstance($obj);

// Getting the value true or false
var_dump($A);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://secure.php.net/manual/en/reflectionclass.isinstance.php](https://secure.php.net/manual/en/reflectionclass.isinstance.php)