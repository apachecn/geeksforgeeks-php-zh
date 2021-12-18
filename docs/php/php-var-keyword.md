# PHP|var 关键字

> Original: [https://www.geeksforgeeks.org/php-var-keyword/](https://www.geeksforgeeks.org/php-var-keyword/)

PHP 中的**var**关键字用于声明默认为**PUBLIC**的类的属性或变量。 声明类的变量或属性时，**var**关键字与**PUBLIC**相同。
**注意：**从 5.0.0 版到 5.1.2 版不建议使用 var 关键字。 从 PHP 5.1.3 开始，它又被添加了一次。
**语法：**和

```
class className {
   var $variable = "GeeksforGeeks";
   // Other statements
}
```

以下程序说明 PHP 中的**var**关键字：
**程序 1：**此程序说明 var 关键字。

## PHP

```
<?php

// Declaring a class
class Geeks {

    // Using var keyword
    // to declare Public variable
    var $var1 = 'Public';

    // Declaring protected variable
    protected $var2 = 'Protected';

    // Declaring private variable
    private $var3 = 'Private';
}

// Creating an object
$obj = new Geeks();

// Calling var declared variable
echo $obj->var1 . "\n";;

?>
```

发帖主题：Re：Колибри0.7.8.0

```
Public
```

**程序 2：**此程序说明了**var**和**public**关键字。

## PHP

```
<?php

// Declaring a class
class Geeks {

    // Using var keyword
    // to declare Public variable
    var $var1 = 'Var Public';

    // Using public keyword
    // to declare Public variable
    public $var2 = 'Public';

}

// Creating an object
$obj = new Geeks();

// Calling var declared variable
echo $obj->var1 . "\n";

// Calling public declared variable
echo $obj->var2 . "\n";;

?>
```

发帖主题：Re：Колибри0.7.8.0

```
Var Public
Public
```

**程序 3：**此程序演示调用私有变量时的错误。

## PHP

```
<?php

// Declaring a class
class Geeks{

    // Using var keyword
    // to declare Public variable
    var $var1 = 'Var Public';

    // Using private keyword
    // to declare private variable
    private $var2 = 'Private';

}

// Creating an object
$obj = new Geeks();

// Calling var declared variable
echo $obj->var1 . "\n";;

// Calling private declared variable
// It will give error
echo $obj->var2 . "\n";;

?>
```

发帖主题：Re：Колибри0.7.8.0

```
Var Public
```

**错误：**和

```
PHP Fatal error:  Uncaught Error: Cannot access private property 
Geeks::$var2 in /home/46488c166fd1197d687867f62e03b8b8.php:24
Stack trace:
#0 {main}
  thrown in /home/46488c166fd1197d687867f62e03b8b8.php on line 24
```