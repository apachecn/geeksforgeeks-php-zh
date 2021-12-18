# PHP|ReflectionClass isCloneable()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-iscloneable-function/](https://www.geeksforgeeks.org/php-reflectionclass-iscloneable-function/)

**ReflectionClass：：isCloneable()函数**是 PHP 中的内置函数，用于检查指定的类是否可克隆。

**语法：**

```php
*bool* ReflectionClass::isCloneable( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果类可克隆，则此函数返回 True，否则返回 False。

下面的程序演示了 PHP 中的 ReflectionClass：：isCloneable()函数：

**程序 1：**

```php
<?php

// Defining a Cloneable class
class Company {
     public function GeeksforGeeks() {}
     public function GFG() {}
}

// Using ReflectionClass over the 
// Cloneable class Company
$B = new ReflectionClass('Company');

// Calling the isCloneable() function
$C = $B->isCloneable();

// Getting the value true or false
var_dump($C);

?>
```

**输出：**

```php
bool(true)

```

**程序 2：**

```php
<?php

// Defining a NotCloneable class
class Alphabets {

    public $A;
    private function __clone() {
    }
}

// Using ReflectionClass over the 
// NotCloneable class Alphabets
$B = new ReflectionClass('Alphabets');

// Calling the isCloneable() function
$C = $B->isCloneable();

// Getting the value true or false
var_dump($C);

?>
```

**输出：**

```php
bool(false)

```

**引用：**[https://www.php.net/manual/en/reflectionclass.iscloneable.php](https://www.php.net/manual/en/reflectionclass.iscloneable.php)