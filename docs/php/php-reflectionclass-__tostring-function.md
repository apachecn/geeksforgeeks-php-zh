# PHP ReflectionClass__toString()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-__tostring-function/](https://www.geeksforgeeks.org/php-reflectionclass-__tostring-function/)

**ReflectionClass__toString()函数**是 PHP 中的内置函数，用于返回指定 ReflectionClass 对象的字符串表示形式。
**语法：**和

```php
*string* ReflectionClass__toString( *void* )
```

**参数：**此函数不接受任何参数。
**返回值：**此函数返回指定 ReflectionClass 对象的字符串表示形式。
以下程序说明 PHP 中的 ReflectionClass__toString()函数：
**程序 1：**和

## PHP

```php
<?php

// Creating a user-defined function
class Alphabets {
    public function A() {}
    public function B() {}
}

// Using ReflectionClass() over the 
// class Alphabets
$class = new ReflectionClass('Alphabets');

// Calling the __toString() function
$A = $class->__toString();

// Getting the string representation
var_dump($A);
?>
```

发帖主题：Re：Колибри0.7.0

> String(435)“Class[<user>class Alphabets]{@@/home/829bc146b7074eafd150c8e57aee5445.php 4-7-Constants[0]{11}-Static Properties[0]{11}-Static Methods[0]{11}-Properties[0]{9}-Methods[2]{Method[<user>public method A]]{@/home/829bc146b707。 /home/829bc146b7074eafd150c8e57aee5445.php 6-6！</user></user>

**程序 2：**

## PHP

```php
<?php

// Using ReflectionClass()
$class = new ReflectionClass('ReflectionClass');

// Calling the __toString() function
$A = $class->__toString();

// Getting the string representation
var_dump($A);
?>
```

发帖主题：Re：Колибри0.7.0

> String(6824)“Class[<reflection>class ReflectionClass 实现反射器]{-Constants[3]{Constant[INTEGER IS_IMPLICIT_ASTRACT]{16}常量[INTEGER IS_EXPLICIT_ASTRACT]{32}ESTANTER[INTEGER IS_FINTAL]{4}*}-静态属性[0]{0}-Static Methods[1]{Method[<reflection prototype="" reflector="">静态公共方法导出]{-Parameters[2]{参数#0[<required>$Argument。 ]参数#1[<optional>$Return]{}{{}}{{}。 。 .Method[<reflection>公共方法 getShortName]{-Parameters[0]{}“</reflection></optional></required></reflection></reflection>

**引用：**[https://www.php.net/manual/en/reflectionclass.tostring.php](https://www.php.net/manual/en/reflectionclass.tostring.php)