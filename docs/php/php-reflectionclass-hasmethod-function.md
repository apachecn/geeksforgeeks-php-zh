# PHP|ReflectionClass hasMethod()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-hasmethod-function/](https://www.geeksforgeeks.org/php-reflectionclass-hasmethod-function/)

**ReflectionClass：：hasMethod()函数**是 PHP 中的内置函数，用于检查指定的方法是否存在。
**语法：**和

```
*bool* ReflectionClass::hasMethod( *string* $name )
```

**参数：**此函数接受单个参数**$name**，该参数保存正在检查的方法的名称。
**返回值：**如果指定的方法存在，则此函数返回 TRUE，否则返回 FALSE。
以下程序说明 PHP：
**程序 1：**和
中的 ReflectionClass：：hasMethod()函数

## PHP

```
<?php

// Initialising a user-defined Class Departments
class Departments {
    public function CSE() { }
    final protected function ECE() { }
    private static function EE() { }
    static function IT() { }
    private function Mechanical() { }
}

// Using ReflectionClass() over the
// user-defined class Departments
$class = new ReflectionClass('Departments');

// Calling the hasMethod() function
$methods = $class->hasMethod('CSE');

// Getting the value true or false
var_dump($methods);
?>
```

**Output:** 

```
bool(true)
```

**程序 2：**和

## PHP

```
<?php

// Initialising a user-defined Class Company
class Company {
    public function GeeksforGeeks() { }
    static function gfg() { }
}

// Using ReflectionClass() over the
// user-defined class Company
$class = new ReflectionClass('Company');

// Calling the hasMethod() function
$methods = $class->hasMethod('TCS');

// Getting the value true or false
var_dump($methods);
?>
```

**Output:** 

```
bool(false)
```

**引用：**[https://php.net/manual/en/reflectionclass.hasmethod.php](https://php.net/manual/en/reflectionclass.hasmethod.php)