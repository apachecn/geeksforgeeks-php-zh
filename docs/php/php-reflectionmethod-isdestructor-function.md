# PHP|ReflectionMethod isDestructor()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionmethod-isdestructor-function/](https://www.geeksforgeeks.org/php-reflectionmethod-isdestructor-function/)

**ReflectionMethod：：isDestructor()函数**是 PHP 中的内置函数，用于在指定的方法是析构函数时返回 true，否则返回 false。

**语法：**

```
*bool* ReflectionMethod::isDestructor( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果指定的方法是析构函数，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明了 PHP 中的 ReflectionMethod：：isDestructor()函数：

**程序 1：**

```
<?php

// Initializing a user-defined class
class Company {
    function __destruct() {}
}

// Using ReflectionMethod() over the class Company
$A = new ReflectionMethod('Company', '__destruct');

// Calling the isDestructor() function
$B = $A->isDestructor();

// Getting the value TRUE if the specified
// method is destructor, otherwise FALSE.
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

    function __destruct() {}
}

class Department3 {
     function marketing(){}
}

// Using ReflectionMethod() over the above classes
$A = new ReflectionMethod('Department1', 'hR');
$B = new ReflectionMethod('Department2', '__destruct');
$C = new ReflectionMethod('Department3', 'marketing');

// Calling the isDestructor() function and 
// getting the value TRUE if the specified
// method is destructor, otherwise FALSE.
var_dump($A->isDestructor());
var_dump($B->isDestructor());
var_dump($C->isDestructor());
?>
```

**输出：**

```
bool(false)
bool(true)
bool(false)

```

**引用：**[https://www.php.net/manual/en/reflectionmethod.isdestructor.php](https://www.php.net/manual/en/reflectionmethod.isdestructor.php)