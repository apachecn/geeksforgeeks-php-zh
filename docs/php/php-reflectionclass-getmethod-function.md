# PHP|ReflectionClass getMethod()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-getmethod-function/](https://www.geeksforgeeks.org/php-reflectionclass-getmethod-function/)

**ReflectionClass：：getMethod()函数**是 PHP 中的内置函数，用于返回指定类方法的 ReflectionMethod。

**语法：**

```
*ReflectionMethod* ReflectionClass::getMethod ( *string* $name )
```

**参数：**此函数接受作为方法名的参数**$name**。

**返回值：**此函数返回指定类方法的 ReflectionMethod。

下面的程序说明 PHP 中的 ReflectionClass：：getMethod()函数：

```
<?php

// Using ReflectionClass over the inbuilt class
// 'ReflectionClass'
$class = new ReflectionClass('ReflectionClass');

// Calling the getMethod over the method named
// as 'getMethod'
$method = $class->getMethod('getMethod');

// Getting the ReflectionMethod for the specified
// inbuilt class method.
var_dump($method);
?>
```

**输出：**

```
object(ReflectionMethod)#2 (2) {
  ["name"]=>
  string(9) "getMethod"
  ["class"]=>
  string(15) "ReflectionClass"
}

```

**引用：**[https://www.php.net/manual/en/reflectionclass.getmethod.php](https://www.php.net/manual/en/reflectionclass.getmethod.php)