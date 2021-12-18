# PHP|ReflectionClass isAnonymous()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-isanonymous-function/](https://www.geeksforgeeks.org/php-reflectionclass-isanonymous-function/)

**ReflectionClass：：isAnonymous()函数**是 PHP 中的一个内置函数，用于检查指定的类是否是匿名的。

**语法：**

```
*bool* ReflectionClass::isAnonymous( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 True，否则返回 False。

下面的程序演示了 PHP 中的 ReflectionClass：：isAnonymous()函数：

**程序 1：**

```
<?php

// Initialising an anonymous class
$anonymousClass = new class {};

// Using ReflectionClass over the anonymous class
$A = new ReflectionClass($anonymousClass);

// Calling the isAnonymous() function
$B = $A->isAnonymous();

// Getting the value true or false
var_dump($B);
?>
```

**输出：**

```
bool(true)

```

**程序 2：**

```
<?php

// Defining a user-defined class Company
class Company {
    private function GeeksforGeeks() {}
    private function GFG() {}
}

// Using ReflectionClass over the
// Company class
$A = new ReflectionClass('Company');

// Calling the isAnonymous() function
$B = $A->isAnonymous();

// Getting the value true or false
var_dump($B);
?>
```

**输出：**

```
bool(false)

```

**引用：**[https://www.php.net/manual/en/reflectionclass.isanonymous.php](https://www.php.net/manual/en/reflectionclass.isanonymous.php)