# PHP ReflectionClass hasProperty()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-hasproperty-function/](https://www.geeksforgeeks.org/php-reflectionclass-hasproperty-function/)

**ReflectionClass hasProperty()函数**是 PHP 中的内置函数，用于检查指定的属性是否存在。

**语法：**

```
*bool* ReflectionClass hasProperty( *string* $name )
```

**参数：**此函数接受单个参数**$name**，该参数保存正在检查的属性的名称。
**返回值：**如果指定的属性存在，则此函数返回 TRUE，否则返回 FALSE。
下面的程序说明了 PHP 中的 ReflectionClass hasProperty()函数：

**程序 1：**

## PHP

```
<?php

// Using ReflectionClass
$ReflectionClass = new ReflectionClass('ReflectionClass');

// Initializing a property name
$a = 'name';

// Calling hasProperty() function over
// the property name
$Property = $ReflectionClass->hasProperty($a);

// Getting the value true or false
var_dump($Property);
?>
```

**Output:** 

```
bool(true)
```