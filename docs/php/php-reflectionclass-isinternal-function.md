# PHP|ReflectionClass isInternal()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-isinternal-function/](https://www.geeksforgeeks.org/php-reflectionclass-isinternal-function/)

**ReflectionClass：：isInternal()函数**是 PHP 中的一个内置函数，用于检查类是由扩展还是核心在内部定义的。

**语法：**

```
*bool* ReflectionClass::isInternal( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果类是由扩展在内部定义的，则此函数返回 TRUE，否则返回 FALSE。

下面的程序演示了 PHP 中的 ReflectionClass：：isInternal()函数：

**程序 1：**

```
<?php

// Initializing a user-defined class Departments
class Departments {
    public function CSE() {}
}

// Using ReflectionClass() over the
// user-defined class Departments
$class = new ReflectionClass('Departments');

// Calling the isInternal() function
$instance = $class->isInternal();

// Getting the value true or false
var_dump($instance);
?>
```

**输出：**

```
bool(false)

```

**程序 2：**

```
<?php

// Using ReflectionClass internally
$InternalClass = new ReflectionClass('ReflectionClass');

// Calling the isInternal() function and
// getting the value true or false
var_dump($InternalClass->isInternal());
?>
```

**输出：**

```
bool(true)

```

**引用：**[https://www.php.net/manual/en/reflectionclass.isinternal.php](https://www.php.net/manual/en/reflectionclass.isinternal.php)