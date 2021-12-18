# PHP|ReflectionParameter__toString()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionparameter-__tostring-function/](https://www.geeksforgeeks.org/php-reflectionparameter-__tostring-function/)

**ReflectionParameter：：__toString()函数**是 PHP 中的内置函数，用于返回指定参数的字符串形式。

**语法：**

```
*string* ReflectionParameter::__toString ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定参数的字符串形式。

以下程序说明 PHP：
**程序 1：**中的**ReflectionParameter：：__toString()**函数

```
<?php

// Initializing a user-defined class Company1
class Company1
{
    public function GFG( $Parameter_1){}
}

// Initializing a subclass Company2
class Company2 extends Company1
{
}

// Using the ReflectionParameter over the above class
$A = new ReflectionParameter(['Company2', 'GFG'], 0); 

// Calling the __toString() function
$B = $A->__toString();

// Getting the string form of the 
// specified parameter.
var_dump($B);
?>
```

发帖主题：Re：Колибри0.7.0

```
string(40) "Parameter #0 [ <required> $Parameter_1 ]"

```

**程序 2：**

```
<?php

// Initializing some user-defined classes
class Department1
{
    function HR( $Full_Name){}
}
class Department2
{
    function Coding( $Parameter2, $Par3 = 'Parameter_3'){}
}
class Department3
{
    function Marketing( &$Parameter4, ...$Parameter5){}
}

// Using the ReflectionParameter over the above classes
$A = new ReflectionParameter(['Department1', 'HR'], 0);
$B = new ReflectionParameter(['Department2', 'Coding'], 1);
$C = new ReflectionParameter(['Department3', 'Marketing'], 1);

// Calling the __toString() function and 
// getting the string form of the 
// specified parameter.
var_dump($A->__toString());
var_dump($B->__toString());
var_dump($C->__toString());
?>
```

发帖主题：Re：Колибри0.7.0

```
string(38) "Parameter #0 [ <required> $Full_Name ]"
string(49) "Parameter #1 [ <optional> $Par3 = 'Parameter_3' ]"
string(42) "Parameter #1 [ <optional> ...$Parameter5 ]"

```

**引用：**[https://www.php.net/manual/en/reflectionparameter.tostring.php](https://www.php.net/manual/en/reflectionparameter.tostring.php)