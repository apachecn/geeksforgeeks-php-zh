# PHP|ReflectionParameter isDefaultValueAvailable()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionparameter-isdefaultvalueavailable-function/](https://www.geeksforgeeks.org/php-reflectionparameter-isdefaultvalueavailable-function/)

ReflectionParameter：：isDefaultValueAvailable()函数是 php 中的一个内置函数，用于在默认值可用时返回 TRUE，否则返回 FALSE

**语法：**

```
*bool* ReflectionParameter::isDefaultValueAvailable ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果有默认值，此函数返回 TRUE，否则返回 FALSE。

下面的程序说明了 php 中的**ReflectionParameter：：isDefaultValueAvailable()函数**：
**程序 1：**

```
<?php

// Initializing a user-defined class Company1
class Company1
{
    function GFG($Full_Name = 'GeeksforGeeks'){}
}

// Initializing a subclass Company2
class Company2 extends Company1
{
}

// Using the ReflectionParameter over the above class
$A = new ReflectionParameter(['Company2', 'GFG'], 0); 

// Calling the isDefaultValueAvailable() function
$B = $A->isDefaultValueAvailable();

// Getting TRUE if a default value is available,
// otherwise FALSE
var_dump($B);
?>
```

发帖主题：Re：Колибри0.7.0

```
bool(true)

```

**程序 2：**

```
<?php

// Initializing some user-defined classes
class Department1
{
    function HR( $Full_Name = 'Human Resource'){}
}
class Department2
{
    function Coding( $Parameter2, $Parameter3){}
}
class Department3
{
    function Marketing( $Parameter4, $Parameter5, $Parameter6){}
}

// Using the ReflectionParameter over the above classes
$A = new ReflectionParameter(['Department1', 'HR'], 0);
$B = new ReflectionParameter(['Department2', 'Coding'], 1);
$C = new ReflectionParameter(['Department3', 'Marketing'], 2);

// Calling the isDefaultValueAvailable() function and 
// getting TRUE if a default value is available, 
// otherwise FALSE
var_dump($A->isDefaultValueAvailable());
var_dump($B->isDefaultValueAvailable());
var_dump($C->isDefaultValueAvailable());
?>
```

发帖主题：Re：Колибри0.7.0

```
bool(true)
bool(false)
bool(false)

```

**引用：**[https://www.php.net/manual/en/reflectionparameter.isdefaultvalueavailable.php](https://www.php.net/manual/en/reflectionparameter.isdefaultvalueavailable.php)