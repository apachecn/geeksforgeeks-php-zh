# PHP|ReflectionExtension getVersion()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionextension-getversion-function/](https://www.geeksforgeeks.org/php-reflectionextension-getversion-function/)

**ReflectionExtension：：getVersion()函数**是 PHP 中的内置函数，用于返回指定扩展的版本。

**语法：**

```php
*string* ReflectionExtension::getVersion( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定扩展的版本。

下面的程序演示了 PHP 中的 ReflectionExtension：：getVersion()函数：

**程序 1：**

```php
<?php

// Defining an extension
$A = 'DOM';

// Using ReflectionExtension() over the 
// specified extension
$extension = new ReflectionExtension($A);

// Calling the getVersion() function
$B = $extension->getVersion();

// Getting the version of the
// specified extension
var_dump($B);
?>
```

**输出：**

```php
string(8) "20031129"

```

**程序 2：**

```php
<?php

// Using ReflectionExtension() over 
// a extension xml
$extension = new ReflectionExtension('xml');

// Calling the getVersion() function and
// Getting the version of the specified extension
var_dump($extension->getVersion());
?>
```

**输出：**

```php
string(23) "7.0.33-0ubuntu0.16.04.7"

```

**引用：**[https://www.php.net/manual/en/reflectionextension.getversion.php](https://www.php.net/manual/en/reflectionextension.getversion.php)