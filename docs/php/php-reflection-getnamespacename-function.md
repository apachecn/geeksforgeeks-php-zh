# PHP|反射 getNamespaceName()函数

> Original: [https://www.geeksforgeeks.org/php-reflection-getnamespacename-function/](https://www.geeksforgeeks.org/php-reflection-getnamespacename-function/)

**Reflation：：getNamespaceName()函数**是 PHP 中的内置函数，用于返回指定名称空间的名称。

**语法：**

```
*string* Reflection::getNamespaceName( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定命名空间的名称。

以下程序说明 PHP：
**程序 1：**中的反射：：getNamespaceName()函数

```
<?php

// Defining a namespace and class GFG
namespace A\B;
class GFG{ } 

// Using ReflectionClass over the namespace and
// specified class GFG
$ReflectionClass = new \ReflectionClass('A\\B\\GFG');

// Calling getNamespaceName() function 
$A = $ReflectionClass->getNamespaceName();

// Getting the name of the specified namespace
var_dump($A);
?>
```

**Output:**

```
string(3) "A\B"

```

**程序 2：**

```
<?php

// Using ReflectionClass over the inbuilt class 'ReflectionClass'
$ReflectionClass = new ReflectionClass('ReflectionClass');

// Calling getNamespaceName() function 
$A = $ReflectionClass->getNamespaceName();

// Getting the name of the namespace
var_dump($A);
?>
```

**Output:**

```
string(0) ""

```

**引用：**[https://www.php.net/manual/en/reflectionclass.getnamespacename.php](https://www.php.net/manual/en/reflectionclass.getnamespacename.php)