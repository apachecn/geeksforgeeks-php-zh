# PHP|ReflectionClass isSubclassOf()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-issubclassof-function/](https://www.geeksforgeeks.org/php-reflectionclass-issubclassof-function/)

**ReflectionClass：：isSubclassOf()函数**是 PHP 中的一个内置函数，用于检查是否有任何子类可用。

**语法：**

```php
*bool* ReflectionClass::isSubclassOf( $class )
```

**参数：**此函数接受单个参数**class**，它是要检查的类名。

**返回值：**如果子类可用，此函数返回 TRUE，否则返回 FALSE。

以下程序说明 PHP：
**程序 1：**中的**ReflectionClass：：isSubclassOf()**函数

```php
<?php

// Initialising a user-defined superclass Company
class Company {
    public function GeeksforGeeks() {}
}

// Creating a subclass Departments 
class Departments extends Company {
    public function HR_Department() {}
}

// Using ReflectionClass() 
$subclass = new ReflectionClass('Departments');

// Calling the isSubclassOf() function
$Result = $subclass->isSubclassOf('Company');

// Getting the value true or false
var_dump($Result);
?>
```

发帖主题：Re：Колибри0.7.0

```php
bool(true)
```

**程序 2：**

```php
<?php

// Initialising a user-defined class Departments
class Departments {
    public function CSE() {}
}

// Using ReflectionClass() over the
// user-defined class Departments
$subclass = new ReflectionClass('Departments');

// Calling the isSubclassOf() function
$Result = $subclass->isSubclassOf('Departments');

// Getting the value true or false
var_dump($Result);
?>
```

发帖主题：Re：Колибри0.7.0

```php
bool(false)
```

**引用：**[https://www.php.net/manual/en/reflectionclass.issubclassof.php](https://www.php.net/manual/en/reflectionclass.issubclassof.php)