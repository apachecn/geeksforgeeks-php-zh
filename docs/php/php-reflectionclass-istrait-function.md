# PHP ReflectionClass isTrait()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-istrait-function/](https://www.geeksforgeeks.org/php-reflectionclass-istrait-function/)

**ReflectionClass isTrait()函数**是 PHP 中的一个内置函数，用于检查是否有任何特征可用。

**语法：**

```
*bool* ReflectionClass isTrait()
```

**参数：**此函数不接受任何参数。
**返回值：**如果特性可用，此函数返回 TRUE，否则返回 FALSE。
下面的程序说明了 PHP 中的**ReflectionClass isTrait()**函数：

**程序 1：**

## PHP

```
<?php

// Defining a trait class
trait Company {
    public function GeeksforGeeks() {
    }
}

// Using ReflectionClass over the
// defined trait
$obj=new ReflectionClass('Company');

// Calling the isTrait() function
$A = $obj->isTrait();

// Getting the value true or false
var_dump($A);
?>
```

发帖主题：Re：Колибри0.7.0

```
bool(true)
```

**程序 2：**

## PHP

```
<?php

// Defining a user-defined class Department
class Department{
}

// Using ReflectionClass over the
// user-defined class Department
$obj=new ReflectionClass('Department');

// Calling the isTrait() function
$Result = $obj->isTrait();

// Getting true or false
var_dump($Result);
?>
```

发帖主题：Re：Колибри0.7.0

```
bool(false)
```

**引用：**[https://www.php.net/manual/en/reflectionclass.istrait.php](https://www.php.net/manual/en/reflectionclass.istrait.php)