# PHP|ReflectionExtension getName()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionextension-getname-function/](https://www.geeksforgeeks.org/php-reflectionextension-getname-function/)

**ReflectionExtension：：getName()函数**是 PHP 中的内置函数，用于返回指定扩展名。

**语法：**

```php
*string* ReflectionExtension::getName( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定扩展名的名称。

下面的程序演示了 PHP 中的 ReflectionExtension：：getName()函数：

**程序 _1：**

```php
<?php

// Defining an extension
$A = 'DOM';

// Using ReflectionExtension() over the 
// specified extension
$extension = new ReflectionExtension($A);

// Calling the getName() function
$B = $extension->getName();

// Getting the name of the
// specified extension
var_dump($B);
?>
```

**输出：**

```php
string(3) "dom"

```

**程序 _2：**

```php
<?php

// Using ReflectionExtension() over 
// a extension xml
$extension = new ReflectionExtension('xml');

// Calling the getName() function and
// Getting the name of the specified extension
var_dump($extension->getName());
?>
```

**输出：**

```php
string(3) "xml"

```

**引用：**[https://www.php.net/manual/en/reflectionextension.getname.php](https://www.php.net/manual/en/reflectionextension.getname.php)