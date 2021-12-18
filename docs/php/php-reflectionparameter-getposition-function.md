# PHP|ReflectionParameter getPosition()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionparameter-getposition-function/](https://www.geeksforgeeks.org/php-reflectionparameter-getposition-function/)

**ReflectionParameter：：getPosition()函数**是 PHP 中的内置函数，用于返回指定参数的位置。

**语法：**

```
*int* ReflectionParameter::getPosition( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定参数的位置。

下面的程序演示了 PHP 中的 ReflectionParameter：：getPosition()函数：

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

// Calling the getPosition() function
$B = $A->getPosition();

// Getting the position of the specified parameter.
var_dump($B);
?>
```

**输出：**

```
int(0)

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
    final function Coding( Exception $Parameter2,
                      Exception $Parameter3){}
}
class Department3
{
    function Marketing($Parameter4, $Parameter5, $Parameter6){}
}

// Using the ReflectionParameter over the above classes
$A = new ReflectionParameter(['Department1', 'HR'], 0);
$B = new ReflectionParameter(['Department2', 'Coding'], 1);
$C = new ReflectionParameter(['Department3', 'Marketing'], 2);

// Calling the getPosition() function and 
// getting the position of the specified parameter
var_dump($A->getPosition());
var_dump($B->getPosition());
var_dump($C->getPosition());
?>
```

**输出：**

```
int(0)
int(1)
int(2)

```

**引用：**[https://secure.php.net/manual/en/reflectionparameter.getposition.php](https://secure.php.net/manual/en/reflectionparameter.getposition.php)