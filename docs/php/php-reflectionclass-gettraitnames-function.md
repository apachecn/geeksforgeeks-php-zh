# PHP|ReflectionClass getTraitNames()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-gettraitnames-function/](https://www.geeksforgeeks.org/php-reflectionclass-gettraitnames-function/)

**ReflectionClass：：getTraitNames()函数**是 PHP 中的一个内置函数，用于返回用户定义类使用的特征名称数组。

**语法：**

```
*array* ReflectionClass::getTraitNames( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回用户定义类使用的特征名称数组。

下面的程序说明了 PHP 中的**ReflectionClass：：getTraitNames()函数**：

**程序 1：**

```
<?php

// Defining a trait class
trait Company {
    public function GeeksforGeeks() {
    }
}

// Defining a user-defined class Department
class Department{
    use Company {
    }
}

// Using ReflectionClass over the
// user-defined class Department
$obj=new ReflectionClass('Department');

// Calling the getTraitNames() function
$A = $obj->getTraitNames();

// Getting an array of names the traits
var_dump($A);
?>
```

**输出：**

```
array(1) {
  [0]=>
  string(7) "Company"
}
```

**程序 2：**

```
<?php

// Defining a user-defined class Department
class Department{
}

// Using ReflectionClass over the
// user-defined class Department
$obj=new ReflectionClass('Department');

// Calling the getTraitNames() function and
// getting an array of name of the traits
var_dump($obj->getTraitNames());
?>
```

**输出：**

```
array(0) {
}
```

**引用：**[https://secure.php.net/manual/en/reflectionclass.gettraitnames.php](https://secure.php.net/manual/en/reflectionclass.gettraitnames.php)