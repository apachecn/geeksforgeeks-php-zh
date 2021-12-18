# PHP|ReflectionClass isUserDefined()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-isuserdefined-function/](https://www.geeksforgeeks.org/php-reflectionclass-isuserdefined-function/)

**ReflectionClass：：isUserDefined()函数**是 PHP 中的一个内置函数，用于检查是否有用户定义的类可用。
**语法：**和

```
*bool* ReflectionClass::isUserDefined()
```

**参数：**此函数不接受任何参数。
**返回值：**如果用户定义的类可用，则此函数返回 TRUE，否则返回 FALSE。
下面的程序说明 PHP：
**程序 1：**和
中的**ReflectionClass：：isUserDefined()**函数

## PHP

```
<?php

// Defining user-defined class Company
Class Company {
    public function GeeksforGeeks() {
    }
}

// Using ReflectionClass over the
// defined class
$obj=new ReflectionClass('Company');

// Calling the isUserDefined() function
$A = $obj->isUserDefined();

// Getting the value true or false
var_dump($A);
?>
```

发帖主题：Re：Колибри0.7.8.0

```
bool(true)
```

**程序 2：**和

## PHP

```
<?php

// Using a internal class 'ReflectionClass'
$obj=new ReflectionClass('ReflectionClass');

// Calling the isUserDefined() function
$A = $obj->isUserDefined();

// Getting the value true or false
var_dump($A);
?>
```

发帖主题：Re：Колибри0.7.8.0

```
bool(false)
```

**引用：**[https://www.php.net/manual/en/reflectionclass.isuserdefined.php](https://www.php.net/manual/en/reflectionclass.isuserdefined.php)