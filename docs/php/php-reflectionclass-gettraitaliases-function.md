# PHP|ReflectionClass getTraitAliases()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-gettraitaliases-function/](https://www.geeksforgeeks.org/php-reflectionclass-gettraitaliases-function/)

**ReflectionClass：：getTraitAliases()函数**是 PHP 中的内置函数，用于返回用户定义类使用的特征别名数组。
**语法：**和

```php
*array* ReflectionClass::getTraitAliases( *void* )
```

**参数：**此函数不接受任何参数。
**返回值：**此函数返回用户定义类使用的特性别名数组。
下面的程序说明 PHP：
**程序 1：**和
中的**ReflectionClass：：getTraitAliases()函数**

## PHP

```php
<?php

// Defining a trait class
trait Company {
    public function GeeksforGeeks() {
    }
}

// Defining a user-defined class Department
class Department{
  use Company {
        Company::GeeksforGeeks as Portal;
    }
}

// Using ReflectionClass over the
// user-defined class Department
$obj=new ReflectionClass('Department');

// Calling the getTraitAliases() function
$A = $obj->getTraitAliases();

// Getting an array of the trait aliases
var_dump($A);
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
array(1) {
  ["Portal"]=>
  string(22) "Company::GeeksforGeeks"
}
```

**程序 2：**和

## PHP

```php
<?php

// Defining a user-defined class Department
class Department{
}

// Using ReflectionClass over the
// user-defined class Department
$obj=new ReflectionClass('Department');

// Calling the getTraitAliases() function and
// getting an array of the trait aliases
var_dump($obj->getTraitAliases());
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
array(0) {
}
```

**引用：**[https://secure.php.net/manual/en/reflectionclass.gettraitaliases.php](https://secure.php.net/manual/en/reflectionclass.gettraitaliases.php)