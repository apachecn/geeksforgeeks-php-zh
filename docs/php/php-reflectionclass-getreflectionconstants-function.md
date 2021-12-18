# PHP|ReflectionClass getReflectionConstants()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-getreflectionconstants-function/](https://www.geeksforgeeks.org/php-reflectionclass-getreflectionconstants-function/)

**ReflectionClass：：getReflectionConstants()函数**是 PHP 中的内置函数，用于返回 ReflectionClassConstant 对象的数组。

**语法：**

```php
*array* ReflectionClass::getReflectionConstants( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回 ReflectionClassConstant 对象的数组。

以下程序说明 PHP：
**程序 1：**中的**ReflectionClass：：getReflectionConstants()函数**

```php
<?php

// Declaring a class named as Company
class Company {

    // Defining some constants
    const First = "GeeksforGeeks";
    const Second = "GFG";
}

// Using the ReflectionClass() function 
// over the Company class
$A = new ReflectionClass('Company');

// Calling the getReflectionConstants() function
$a = $A->getReflectionConstants();

// Getting an array of ReflectionClassConstant objects.
print_r($a);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array
(
    [0] => ReflectionClassConstant Object
        (
            [name] => First
            [class] => Company
        )

    [1] => ReflectionClassConstant Object
        (
            [name] => Second
            [class] => Company
        )

)

```

**程序 2：**

```php
<?php

// Using the ReflectionClass() function 
$A = new ReflectionClass('ReflectionClass');

// Calling the getReflectionConstants() function
$a = $A->getReflectionConstants();

// Getting an array of ReflectionClassConstant objects.
print_r($a);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array
(
    [0] => ReflectionClassConstant Object
        (
            [name] => IS_IMPLICIT_ABSTRACT
            [class] => ReflectionClass
        )

    [1] => ReflectionClassConstant Object
        (
            [name] => IS_EXPLICIT_ABSTRACT
            [class] => ReflectionClass
        )

    [2] => ReflectionClassConstant Object
        (
            [name] => IS_FINAL
            [class] => ReflectionClass
        )

)
```

**引用：**[https://secure.php.net/manual/en/reflectionclass.getreflectionconstants.php](https://secure.php.net/manual/en/reflectionclass.getreflectionconstants.php)