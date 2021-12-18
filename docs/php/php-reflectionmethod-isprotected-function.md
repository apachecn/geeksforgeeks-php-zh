# PHP|ReflectionMethod isProtected()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionmethod-isprotected-function/](https://www.geeksforgeeks.org/php-reflectionmethod-isprotected-function/)

**ReflectionMethod：：isProtected()函数**是 PHP 中的一个内置函数，用于在指定的方法受保护时返回 TRUE，否则返回 FALSE。

**语法：**

```
*bool* ReflectionMethod::isProtected ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果指定的方法受保护，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明了 PHP 中的 ReflectionMethod：：isProtected()函数：

**程序 1：**

```
<?php

// Initializing a user-defined class
class Company {
    protected function GFG() {}
}

// Using ReflectionMethod() over the class Company
$A = new ReflectionMethod('Company', 'GFG');

// Calling the isProtected() function
$B = $A->isProtected();

// Getting the value TRUE if the specified
// method is protected, otherwise FALSE.
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
    protected function Coding() {}
}

class Department3 {
     function marketing(){}
}

// Using ReflectionMethod() over the above classes
$A = new ReflectionMethod('Department1', 'hR');
$B = new ReflectionMethod('Department2', 'Coding');
$C = new ReflectionMethod('Department3', 'marketing');

// Calling the isProtected() function and 
// getting the value TRUE if the specified
// method is protected, otherwise FALSE.
var_dump($A->isProtected());
var_dump($B->isProtected());
var_dump($C->isProtected());
?>
```

**输出：**

```
bool(false)
bool(true)
bool(false)

```

**引用：**[https://www.php.net/manual/en/reflectionmethod.isprotected.php](https://www.php.net/manual/en/reflectionmethod.isprotected.php)