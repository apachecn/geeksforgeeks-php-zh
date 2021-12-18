# PHP|ReflectionParameter hasType()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionparameter-hastype-function/](https://www.geeksforgeeks.org/php-reflectionparameter-hastype-function/)

**ReflectionParameter：：hasType()函数**是 PHP 中的一个内置函数，用于在指定类型时返回 true，否则返回 false。

**语法：**

```
*bool* ReflectionParameter::hasType ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果指定了类型，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明 PHP：
**程序 1：**中的**ReflectionParameter：：hasType()函数**

```
<?php

// Initializing a user-defined class Company1
class Company1
{
    public function GFG( int $Parameter){}
}

// Initializing a subclass Company2
class Company2 extends Company1
{
}

// Using the ReflectionParameter over the above class
$A = new ReflectionParameter(['Company2', 'GFG'], 0); 

// Calling the hasType() function
$B = $A->hasType();

// Getting TRUE if a type is specified, 
// FALSE otherwise.
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
    protected function HR(float $Parameter1){}
}
class Department2
{
    final function Coding( $Parameter2, $Parameter3){}
}
class Department3
{
    function Marketing( sting $Parameter4, 
      string $Parameter5, string $Parameter6){}
}

// Using the ReflectionParameter over the above classes
$A = new ReflectionParameter(['Department1', 'HR'], 0);
$B = new ReflectionParameter(['Department2', 'Coding'], 1);
$C = new ReflectionParameter(['Department3', 'Marketing'], 2);

// Calling the hasType() function and 
// getting TRUE if a type is specified, 
// FALSE otherwise.
var_dump($A->hasType());
var_dump($B->hasType());
var_dump($C->hasType());
?>
```

发帖主题：Re：Колибри0.7.0

```
bool(true)
bool(false)
bool(true)

```

**引用：**[https://www.php.net/manual/en/reflectionparameter.hastype.php](https://www.php.net/manual/en/reflectionparameter.hastype.php)