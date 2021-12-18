# PHP|ReflectionExtension info()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionextension-info-function/](https://www.geeksforgeeks.org/php-reflectionextension-info-function/)

**ReflectionExtension：：Info()函数**是 PHP 中的内置函数，用于返回指定扩展的信息。

**语法：**

```
*void* ReflectionExtension::info( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定分机的信息。

以下程序说明了 PHP 中的 ReflectionExtension：：Info()函数：

**程序 1：**

```
<?php

// Defining an extension
$A = 'DOM';

// Using ReflectionExtension() over the 
// specified extension
$extension = new ReflectionExtension($A);

// Calling the info() function
$B = $extension->info();

// Getting the information of the
// specified extension
var_dump($B);
?>
```

**输出：**

```
dom

DOM/XML => enabled
DOM/XML API Version => 20031129
libxml Version => 2.9.3
HTML Support => enabled
XPath Support => enabled
XPointer Support => enabled
Schema Support => enabled
RelaxNG Support => enabled
NULL

```

**程序 2：**

```
<?php

// Using ReflectionExtension() over 
// a extension xml
$extension = new ReflectionExtension('xml');

// Calling the info() function and
// Getting the information of the specified extension
var_dump($extension->info());
?>
```

**输出：**

```
xml

XML Support => active
XML Namespace Support => active
libxml2 Version => 2.9.3
NULL

```

**引用：**[https://www.php.net/manual/en/reflectionextension.info.php](https://www.php.net/manual/en/reflectionextension.info.php)