# PHP|ReflectionParameter getType()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionparameter-gettype-function/](https://www.geeksforgeeks.org/php-reflectionparameter-gettype-function/)

**ReflectionParameter：：getType()函数**是 PHP 中的内置函数，用于返回指定参数的类型。

**语法：**

```php
*ReflectionType* ReflectionParameter::getType ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定参数的类型。

下面的程序演示了 PHP 中的 ReflectionParameter：：getType()函数：

**程序 1：**

```php
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

// Calling the getType() function
$B = $A->getType();

// Getting the type of the specified parameter.
echo $B;
?>
```

**输出：**

```php
int

```

**程序 2：**

```php
<?php

// Initializing some user-defined classes
class Department1
{
    protected function HR(float $Parameter1){}
}
class Department2
{
    final function Coding( Exception $Parameter2,
                Exception $Parameter3){}
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

// Calling the getType() function and 
// getting the type of the specified parameter
echo $A->getType();
echo "\n";
echo $B->getType();
echo "\n";
echo $C->getType();
?>
```

**输出：**

```php
float
Exception
string

```

**引用：**[https://secure.php.net/manual/en/reflectionparameter.gettype.php](https://secure.php.net/manual/en/reflectionparameter.gettype.php)