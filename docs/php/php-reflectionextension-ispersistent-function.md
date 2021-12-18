# PHP|ReflectionExtension isPersistent()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionextension-ispersistent-function/](https://www.geeksforgeeks.org/php-reflectionextension-ispersistent-function/)

**ReflectionExtension：：isPersistent()函数**是 PHP 中的内置函数，用于在指定的扩展是持久的时返回 TRUE，否则返回 FALSE。

**语法：**

```php
*void* ReflectionExtension::isPersistent( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果指定的扩展是持久的，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明了 PHP 中的 ReflectionExtension：：isPersistent()函数：

**程序 _1：**

```php
<?php

// Defining an extension
$A = 'DOM';

// Using ReflectionExtension() over the 
// specified extension
$extension = new ReflectionExtension($A);

// Calling the isPersistent() function
$B = $extension->isPersistent();

// Getting the value either true or false
var_dump($B);
?>
```

**输出：**

```php
bool(true)

```

**程序 _2：**

```php
<?php

// Using ReflectionExtension() over 
// an extension xml
$extension = new ReflectionExtension('xml');

// Calling the isPersistent() function and
// Getting the value either true or false
var_dump($extension->isPersistent());
?>
```

**输出：**

```php
bool(true)

```

**引用：**[https://www.php.net/manual/en/reflectionextension.ispersistent.php](https://www.php.net/manual/en/reflectionextension.ispersistent.php)