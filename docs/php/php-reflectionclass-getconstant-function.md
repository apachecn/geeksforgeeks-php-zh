# PHP|ReflectionClass getConstant()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionclass-getconstant-function/](https://www.geeksforgeeks.org/php-reflectionclass-getconstant-function/)

**ReflectionClass：：getConstant()函数**是 PHP 中的内置函数，用于返回定义的常量的值。

**语法：**

```
*mixed* ReflectionClass::getConstant( *string* $name )
```

**参数：**此函数接受参数**名称**，它是定义的常量的名称。

**返回值：**此函数返回定义的常量的值。

下面的程序演示了 PHP 中的*ReflectionClass：：getConstant()函数*：

**程序 1：**

```
<?php

// Declaring a class named as Department
class Department {

    // Defining a constant
    const First = "CSE";

}

// Using the ReflectionClass() function 
// over the Department class
$A = new ReflectionClass('Department');

// Calling the getConstant() function over
// First constant
$a = $A->getConstant('First');

// Getting the value of the defined constant
print_r($a);
?>
```

**输出：**

```
CSE

```

**程序 2：**

```
<?php

// Declaring a class named as Company
class Company {

    // Defining a constant
    const First = "GeeksforGeeks";
    const Second = "GFG";
    const Third = "gfg";

}

// Using the ReflectionClass() function 
// over the Company class
$A = new ReflectionClass('Company');

// Calling the getConstant() function over
// the defined constants and
// getting the value of the defined constants
print_r($A->getConstant('First'));
echo("\n");
print_r($A->getConstant('Second'));
echo("\n");
print_r($A->getConstant('Third'));
?>
```

**输出：**

```
GeeksforGeeks
GFG
gfg

```

**引用：**[https://www.php.net/manual/en/reflectionclass.getconstant.php](https://www.php.net/manual/en/reflectionclass.getconstant.php)