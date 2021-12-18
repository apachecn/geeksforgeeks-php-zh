# PHP|ReflectionExtension isTemporary()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionextension-istemporary-function/](https://www.geeksforgeeks.org/php-reflectionextension-istemporary-function/)

**ReflectionExtension：：isTemporary()函数**是 PHP 中的一个内置函数，用于在指定的扩展是临时的时返回 TRUE，否则返回 FALSE。

**语法：**

```php
*void* ReflectionExtension::isTemporary( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果指定的扩展是临时的，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明了 PHP 中的 ReflectionExtension：：isTemporary()函数：

**程序 1：**

```php
<?php

// Defining an extension
$A = 'DOM';

// Using ReflectionExtension() over the 
// specified extension
$extension = new ReflectionExtension($A);

// Calling the isTemporary() function
$B = $extension->isTemporary();

// Getting the value either true or false
var_dump($B);
?>
```

**输出：**

```php
bool(false)

```

**程序 2：**

```php
<?php

// Using ReflectionExtension() over 
// an extension xml
$extension = new ReflectionExtension('xml');

// Calling the isTemporary() function and
// Getting the value either true or false
var_dump($extension->isTemporary());
?>
```

**输出：**

```php
bool(false)

```

**引用：**[https://www.php.net/manual/en/reflectionextension.istemporary.php](https://www.php.net/manual/en/reflectionextension.istemporary.php)