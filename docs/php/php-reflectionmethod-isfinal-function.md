# PHP|ReflectionMethod isFinal()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionmethod-isfinal-function/](https://www.geeksforgeeks.org/php-reflectionmethod-isfinal-function/)

**ReflectionMethod：：isFinal()函数**是 PHP 中的内置函数，用于在指定方法为 Final 时返回 True，否则返回 False。

**语法：**

```
*bool* ReflectionMethod::isFinal( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果指定的方法是最终的，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明了 PHP 中的 ReflectionMethod：：isFinal()函数：

**程序 1：**

```
<?php

// Initializing a user-defined class
class Company {

    final function GFG() {}
}

// Using ReflectionMethod() over the class Company
$A = new ReflectionMethod('Company', 'GFG');

// Calling the isFinal() function
$B = $A->isFinal();

// Getting the value TRUE if the specified
// method is final, otherwise FALSE.
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

// Initializing some user-defined classes
class Department1 {

    public function hr($name) {
        return 'HR' . $name;
    }
}
class Department2 {

    final function Coding() {}
}

class Department3 {

     function marketing(){}
}

// Using ReflectionMethod() over the above classes
$A = new ReflectionMethod('Department1', 'hR');
$B = new ReflectionMethod('Department2', 'Coding');
$C = new ReflectionMethod('Department3', 'marketing');

// Calling the isFinal() function and 
// getting the value TRUE if the specified
// method is final, otherwise FALSE.
var_dump($A->isFinal());
var_dump($B->isFinal());
var_dump($C->isFinal());
?>
```

**输出：**

```
bool(false)
bool(true)
bool(false)

```

**引用：**[https://www.php.net/manual/en/reflectionmethod.isfinal.php](https://www.php.net/manual/en/reflectionmethod.isfinal.php)