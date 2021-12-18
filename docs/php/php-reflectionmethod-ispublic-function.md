# PHP|ReflectionMethod isPublic()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionmethod-ispublic-function/](https://www.geeksforgeeks.org/php-reflectionmethod-ispublic-function/)

**ReflectionMethod：：isPublic()函数**是 PHP 中的一个内置函数，用于在指定的方法为公共方法时返回 true，否则返回 false。

**语法：**

```
*bool* ReflectionMethod::isPublic ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果指定的方法是公共的，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明 PHP：
**程序 1：**中的**ReflectionMethod：：isPublic()函数**

```
<?php

// Initializing a user-defined class
class Company {

    public function GFG() {}
}

// Using ReflectionMethod() over the class Company
$A = new ReflectionMethod('Company', 'GFG');

// Calling the isPublic() function
$B = $A->isPublic();

// Getting the value TRUE if the specified
// method is public, otherwise FALSE.
var_dump($B);
?>
```

发帖主题：Re：Колибри0.7.0

```
bool(true)

```

**程序 2：**

```
<?php

// Initializing some user-defined classes
class Department1 {

    private function hr($name) {
        return 'HR' . $name;
    }
}
class Department2 {

    public function Coding() {}
}

class Department3 {

     protected function marketing(){}
}

// Using ReflectionMethod() over the above classes
$A = new ReflectionMethod('Department1', 'hR');
$B = new ReflectionMethod('Department2', 'Coding');
$C = new ReflectionMethod('Department3', 'marketing');

// Calling the isPublic() function and 
// getting the value TRUE if the specified
// method is public, otherwise FALSE.
var_dump($A->isPublic());
var_dump($B->isPublic());
var_dump($C->isPublic());
?>
```

发帖主题：Re：Колибри0.7.0

```
bool(false)
bool(true)
bool(false)

```

**引用：**[https://www.php.net/manual/en/reflectionmethod.ispublic.php](https://www.php.net/manual/en/reflectionmethod.ispublic.php)