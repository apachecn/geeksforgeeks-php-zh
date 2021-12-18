# PHP|ReflectionParameter canBePassedByValue()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionparameter-canbepassedbyvalue-function/](https://www.geeksforgeeks.org/php-reflectionparameter-canbepassedbyvalue-function/)

**ReflectionParameter：：canBePassedByValue()函数**是 PHP 中的一个内置函数，用于在参数可以通过值传递时返回 TRUE，否则返回 FALSE。

**语法：**

```
*bool* ReflectionParameter::canBePassedByValue( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果参数可以通过值传递，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明了 PHP 中的 ReflectionParameter：：canBePassedByValue()函数：

**程序 1：**

```
<?php

// Initializing a user-defined class Company1
class Company1
{
    public function GFG( $Parameter){}
}

// Initializing a subclass Company2
class Company2 extends Company1
{
}

// Using the ReflectionParameter over the above class
$A = new ReflectionParameter(['Company2', 'GFG'], 0); 

// Calling the canBePassedByValue() function
$B = $A->canBePassedByValue();

// Getting the boolean value TRUE if the 
// parameter can be passed by value, 
// otherwise returns FALSE. 
var_dump($B);
?>
```

**输出：**

```
bool(true)

```

**程序 2：**

```
<?php

// Initializing some user-defined classes
class Department1
{
    protected function HR($Parameter1){}
}
class Department2
{
    final function Coding( Exception $Parameter2, Exception $Parameter3){}
}
class Department3
{
    function Marketing($Parameter4, $Parameter5, $Parameter6){}
}

// Using the ReflectionParameter over the above classes
$A = new ReflectionParameter(['Department1', 'HR'], 0);
$B = new ReflectionParameter(['Department2', 'Coding'], 1);
$C = new ReflectionParameter(['Department3', 'Marketing'], 2);

// Calling the canBePassedByValue() function and
// getting the boolean value TRUE if the 
// parameter can be passed by value, 
// otherwise returns FALSE. 
var_dump($A->canBePassedByValue());
var_dump($B->canBePassedByValue());
var_dump($C->canBePassedByValue());
?>
```

**输出：**

```
bool(true)
bool(true)
bool(true)

```

**引用：**[https://secure.php.net/manual/en/reflectionparameter.canbepassedbyvalue.php](https://secure.php.net/manual/en/reflectionparameter.canbepassedbyvalue.php)