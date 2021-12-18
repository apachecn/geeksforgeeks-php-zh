# PHP|ReflectionMethod getClosure()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionmethod-getclosure-function/](https://www.geeksforgeeks.org/php-reflectionmethod-getclosure-function/)

**ReflectionMethod：：getClosure()函数**是 PHP 中的一个内置函数，用于为该方法返回动态创建的闭包，否则在出错时返回 NULL。

**语法：**

```php
*Closure* ReflectionMethod::getClosure ( *$object* )
```

**参数：**此函数接受参数**对象**，它是指定的用户定义类对象。

**返回值：**此函数返回为该方法动态创建的闭包，否则在出错时返回 NULL。

下面的程序说明了 PHP 中的**ReflectionMethod：：getClosure()函数**：

**程序 _1：**

## PHP

```php
<?php

// Initializing a user-defined class
class Company {

    protected function GeeksforGeeks($name) {
        return 'GFG' . $name;
    }
}

// Using ReflectionMethod() over the class Company
$A = new ReflectionMethod('Company', 'GeeksforGeeks');

// Calling the getClosure() function
$B = $A->getClosure(new Company());

// Getting a dynamically created closure
// for the method otherwise, return NULL
// in case of an error.
var_dump($B);
?>
```

**Output:** 

```php
object(Closure)#3 (2) {
  ["this"]=>
  object(Company)#2 (0) {
  }
  ["parameter"]=>
  array(1) {
    ["$name"]=>
    string(10) "<required>"
  }
}
```

**程序 _2：**

## PHP

```php
<?php

// Initializing some user-defined classes
class Department1 {

    protected function HR($name) {
        return 'hr' . $name;
    }
}
class Department2 {

    protected function Coding($name) {
        return 'coding' . $name;
    }
}
class Department3 {

    protected function Marketing($name) {
        return 'marketing' . $name;
    }
}

// Using ReflectionMethod() over the above classes
$A = new ReflectionMethod('Department1', 'HR');
$B = new ReflectionMethod('Department2', 'Coding');
$C = new ReflectionMethod('Department3', 'Marketing');

// Calling the getClosure() function and
// Getting a dynamically created closure
// for the method otherwise, return NULL
// in case of an error.
var_dump($A->getClosure(new Department1()));
var_dump($B->getClosure(new Department2()));
var_dump($C->getClosure(new Department3()));
?>
```

**Output:** 

```php
object(Closure)#5 (2) {
  ["this"]=>
  object(Department1)#4 (0) {
  }
  ["parameter"]=>
  array(1) {
    ["$name"]=>
    string(10) "<required>"
  }
}
object(Closure)#4 (2) {
  ["this"]=>
  object(Department2)#5 (0) {
  }
  ["parameter"]=>
  array(1) {
    ["$name"]=>
    string(10) "<required>"
  }
}
object(Closure)#5 (2) {
  ["this"]=>
  object(Department3)#4 (0) {
  }
  ["parameter"]=>
  array(1) {
    ["$name"]=>
    string(10) "<required>"
  }
}
```

**引用：**[https://www.php.net/manual/en/reflectionmethod.getclosure.php](https://www.php.net/manual/en/reflectionmethod.getclosure.php)