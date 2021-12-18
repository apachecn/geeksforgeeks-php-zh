# PHP|ReflectionParameter getDefaultValueConstantName()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionparameter-getdefaultvalueconstantname-function/](https://www.geeksforgeeks.org/php-reflectionparameter-getdefaultvalueconstantname-function/)

**ReflectionParameter：：getDefaultValueConstantName()函数**是 php 中的一个内置函数，用于在缺省值为 Constant 或 NULL 时返回缺省值的常量名称。

**语法：**

```
 *string* ReflectionParameter::getDefaultValueConstantName ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果默认值为 Constant 或 NULL，则此函数返回默认值的常量名称。

下面的程序说明了 php 中的**ReflectionParameter：：getDefaultValueConstantName()函数**：
**程序 1：**

```
<?php

// Initializing a user-defined class Company1
class Company1
{
    function GFG($Full_Name = GeeksforGeeks){}
}

// Initializing a subclass Company2
class Company2 extends Company1
{
}

// Using the ReflectionParameter over the above class
$A = new ReflectionParameter(['Company2', 'GFG'], 0); 

// Calling the getDefaultValueConstantName() function
$B = $A->getDefaultValueConstantName();

// Getting the default value's constant name 
// if default value is constant or null
var_dump($B);
?>
```

发帖主题：Re：Колибри0.7.0

```
string(13) "GeeksforGeeks"

```

**程序 2：**

```
<?php

// Initializing some user-defined classes
class Department1
{
    function HR( $Full_Name = Human_Resource){}
}
class Department2
{
    function Coding( $Parameter2, $Par3 = Parameter3){}
}
class Department3
{
    function Marketing( $Parameter4 = Digital_Marketing, $Parameter5){}
}

// Using the ReflectionParameter over the above classes
$A = new ReflectionParameter(['Department1', 'HR'], 0);
$B = new ReflectionParameter(['Department2', 'Coding'], 1);
$C = new ReflectionParameter(['Department3', 'Marketing'], 0);

// Calling the getDefaultValueConstantName() function and 
// getting the default value's constant name if 
// default value is constant or null
var_dump($A->getDefaultValueConstantName());
var_dump($B->getDefaultValueConstantName());
var_dump($C->getDefaultValueConstantName());
?>
```

发帖主题：Re：Колибри0.7.0

```
string(14) "Human_Resource"
string(10) "Parameter3"
string(17) "Digital_Marketing"

```

**引用：**[https://www.php.net/manual/en/reflectionparameter.getdefaultvalueconstantname.php](https://www.php.net/manual/en/reflectionparameter.getdefaultvalueconstantname.php)