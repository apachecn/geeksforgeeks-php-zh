# PHP|ReflectionMethod__toString()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionmethod-__tostring-function/](https://www.geeksforgeeks.org/php-reflectionmethod-__tostring-function/)

**ReflectionMethod：：__toString()函数**是 PHP 中的内置函数，用于返回指定方法对象的字符串表示形式。

**语法：**

```php
*string* ReflectionMethod::__toString ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定方法对象的字符串表示形式。

以下程序说明 PHP：
**程序 1：**中的**ReflectionMethod：：__toString()函数**

```php
<?php

// Initializing a user-defined class
class Company {

     function GFG() {}
}

// Using ReflectionMethod() over the class Company
$A = new ReflectionMethod('Company', 'GFG');

// Calling the __toString() function
$B = $A->__toString();

// Getting the string representation of 
// the specified method object 'GFG'
var_dump($B);
?>
```

发帖主题：Re：Колибри0.7.0

```php
string(94) "Method [ <user> public method GFG ] {
  @@ /home/43d46426def0fce620e2e2cf2bf10e7a.php 6 - 6
}
"

```

**程序 2：**

```php
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

// Calling the __toString() function and 
// getting the string representation of the
// above method objects
var_dump($A->__toString());
var_dump($B->__toString());
var_dump($C->__toString());
?>
```

发帖主题：Re：Колибри0.7.0

```php
string(158) "Method [ <user> private method hr ] {
  @@ /home/2aa9608c9056b85288d53e96d9de3310.php 6 - 8

  - Parameters [1] {
    Parameter #0 [ <required> $name ]
  }
}
"
string(106) "Method [ <user> static public method Coding ] {
  @@ /home/2aa9608c9056b85288d53e96d9de3310.php 12 - 12
}
"
string(105) "Method [ <user> protected method marketing ] {
  @@ /home/2aa9608c9056b85288d53e96d9de3310.php 17 - 17
}
"

```

**引用：**[https://www.php.net/manual/en/reflectionmethod.tostring.php](https://www.php.net/manual/en/reflectionmethod.tostring.php)