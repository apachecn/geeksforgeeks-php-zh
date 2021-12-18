# PHP |类

> 原文:[https://www.geeksforgeeks.org/php-classes/](https://www.geeksforgeeks.org/php-classes/)

像[c++](https://www.geeksforgeeks.org/c-plus-plus/)[Java](https://www.geeksforgeeks.org/java/)[PHP](https://www.geeksforgeeks.org/php/)也支持面向对象编程

1.  类是对象的蓝图。函数和类之间的一个很大的区别是，一个类包含数据(变量)和函数，它们组成了一个名为“对象”的包。
2.  类是程序员定义的数据类型，包括局部方法和局部变量。
3.  类是对象的集合。对象具有属性和行为。

**语法:**我们定义自己的类，从关键字**‘类’**开始，然后是你想给你的新类取的名字。

```php
<?php 
    class person {

    }
?>
```

**注意:**我们用花括号 **( { } )** 括起一个类……就像你用函数一样。

下面给出的程序详细说明了 PHP 中面向对象编程中**类**的使用。
这些程序将举例说明文章中给出的例子。

**程序 1:**

```php
<?php
class GeeksforGeeks
{
    // Constructor
    public function __construct(){
        echo 'The class "' . __CLASS__ . '" was initiated!<br>';
    }

}

// Create a new object
$obj = new GeeksforGeeks;
?>
```

**输出**:

```php
The class "GeeksforGeeks" was initiated.
```

**程序 2:**

```php
<?php
class GeeksforGeeks
{
    // Destructor
    public function __destruct(){
        echo 'The class "' . __CLASS__ . '" was destroyed!';
    }

}

// Create a new object
$obj = new GeeksforGeeks;
?>
```

**输出:**

```php
The class "GeeksforGeeks" was destroyed.

```

**参考:**
[PHP 中的类](http://php.net/manual/en/language.oop5.basic.php)