# PHP|ReflectionMethod isStatic()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionmethod-isstatic-function/](https://www.geeksforgeeks.org/php-reflectionmethod-isstatic-function/)

**ReflectionMethod：：isStatic()函数**是 PHP 中的一个内置函数，用于在指定的方法是静态的时返回 true，否则返回 false。

**语法：**

```
*public bool* ReflectionMethod::isStatic ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果指定的方法是静态的，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明 PHP：
**程序 1：**中的**ReflectionMethod：：isStatic()函数**

```
<?php

// Initializing a user-defined class
class Company {

    static function GFG() {}
}

// Using ReflectionMethod() over the class Company
$A = new ReflectionMethod('Company', 'GFG');

// Calling the isStatic() function
$B = $A->isStatic();

// Getting the value TRUE if the specified
// method is static, otherwise FALSE.
var_dump($B);
?>
```

发帖主题：Re：Колибри0.7.0

```
bool(true)

```

**程序 _2：**

```
<?php

// Initializing some user-defined classes
class Department1 {

    private function hr($name) {
        return 'HR' . $name;
    }
}
class Department2 {

    static function Coding() {}
}

class Department3 {

     protected function marketing(){}
}

// Using ReflectionMethod() over the above classes
$A = new ReflectionMethod('Department1', 'hR');
$B = new ReflectionMethod('Department2', 'Coding');
$C = new ReflectionMethod('Department3', 'marketing');

// Calling the isStatic() function and 
// getting the value TRUE if the specified
// method is static, otherwise FALSE.
var_dump($A->isStatic());
var_dump($B->isStatic());
var_dump($C->isStatic());
?>
```

发帖主题：Re：Колибри0.7.0

```
bool(false)
bool(true)
bool(false)

```

**引用：**[https://www.php.net/manual/en/reflectionmethod.isstatic.php](https://www.php.net/manual/en/reflectionmethod.isstatic.php)