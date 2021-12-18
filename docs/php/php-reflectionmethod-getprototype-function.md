# PHP|ReflectionMethod getPrototype()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionmethod-getprototype-function/](https://www.geeksforgeeks.org/php-reflectionmethod-getprototype-function/)

**ReflectionMethod：：getPrototype()函数**是 PHP 中的内置函数，用于返回指定方法的原型，否则，如果该方法没有原型，则返回异常/错误。

**语法：**

```php
*ReflectionMethod* ReflectionMethod::getPrototype( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定方法的原型，否则，如果该方法没有原型，则返回异常/错误。

以下程序说明 PHP：
**程序 1：**中的 ReflectionMethod：：getPrototype()函数

```php
<?php

// Initializing a user-defined class Department1
class Department1 {

    public function Marketing_Dpt() {
        return 'Department1';
    }
}

// Initializing a subclass of the above class Department1
class Department2 extends Department1{

    public function Marketing_Dpt() {
        return 'Department2';
    }

}

// Again Initializing a subclass of the above subclass Department2
class Department3 extends Department2{

    public function Coding_Dpt() {
        return 'Department3';
    }

}

// Using the ReflectionMethod() over the above 
// subclass Department2
$A = new ReflectionMethod('Department3', 'Marketing_Dpt');

// Calling the getPrototype() function
$B = $A->getPrototype();

// Getting the prototype 
var_dump($B);
?>
```

发帖主题：Re：Колибри0.7.0

```php
object(ReflectionMethod)#2 (2) {
  ["name"]=>
  string(13) "Marketing_Dpt"
  ["class"]=>
  string(11) "Department1"
}

```

**程序 2：**

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

// Calling the getPrototype() function
$B = $A->getPrototype();

// Getting the prototype or an error is returned
// if the method does not have a prototype.
var_dump($B);
?>
```

**输出：**方法没有任何会给您带来错误的原型。

```php
PHP Fatal error: Uncaught ReflectionException: Method Company::
GeeksforGeeks does not have a prototype in 
/home/9d8367b263ee4d7ec6941876b0eae792.php:15
Stack trace:
#0 /home/9d8367b263ee4d7ec6941876b0eae792.php(15): 
ReflectionMethod->getPrototype()
#1 {main}
  thrown in /home/9d8367b263ee4d7ec6941876b0eae792.php on line 15

```

**引用：**[https://www.php.net/manual/en/reflectionmethod.getprototype.php](https://www.php.net/manual/en/reflectionmethod.getprototype.php)