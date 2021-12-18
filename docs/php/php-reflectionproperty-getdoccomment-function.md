# PHP|ReflectionProperty getDocComment()函数

> Original: [https://www.geeksforgeeks.org/php-reflectionproperty-getdoccomment-function/](https://www.geeksforgeeks.org/php-reflectionproperty-getdoccomment-function/)

**ReflectionProperty：：getDocComment()函数**是 PHP 中的内置函数，用于返回指定属性的文档注释。

**语法：**

```php
*string* ReflectionProperty::getDocComment ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定属性的单据备注。

以下程序说明 PHP：
**程序 1：**中的 ReflectionProperty：：getDocComment()函数

```php
<?php

// Initializing a user-defined class Company
class Company
{
    /**
     * @Below is the Size of GeeksforGeeks String
     */
    public $SizeOfGeeksforGeeks = 13;

    /**
     * @Below is the Size of GFG String
     */
    public $SizeOfGFG = 3;
}

// Using ReflectionProperty 
$A = new ReflectionProperty('Company', 'SizeOfGeeksforGeeks');
$B = new ReflectionProperty('Company', 'SizeOfGFG');

// Calling the getDocComment() function
$C = $A->getDocComment();
$D = $B->getDocComment();

// Getting the doc comment of the specified property
var_dump($C);
var_dump($D);
?>
```

发帖主题：Re：Колибри0.7.0

```php
string(63) "/**
     * @Below is the Size of GeeksforGeeks String
     */"
string(53) "/**
     * @Below is the Size of GFG String
     */"

```

**程序 2：**

```php
<?php

// Initializing some user-defined classes
class Department1
{
    /**
     * @Below is the Size of HR String
     */
    public $SizeOfHR = 2;
}
class Department2
{
    /**
     * @Below is the Size of Coding String
     */
    public $SizeOfCoding = 6;
}
class Department3
{
    /**
     * @Below is the Size of Marketing String
     */
    public $SizeOfMarketing = 9;
}

// Using ReflectionProperty over above classes
$A = new ReflectionProperty('Department1', 'SizeOfHR');
$B = new ReflectionProperty('Department2', 'SizeOfCoding');
$C = new ReflectionProperty('Department3', 'SizeOfMarketing');

// Calling the getDocComment() function
$D = $A->getDocComment();
$E = $B->getDocComment();
$F = $C->getDocComment();

// Getting the doc comments of the specified properties
var_dump($D);
var_dump($E);
var_dump($F);
?>
```

发帖主题：Re：Колибри0.7.0

```php
string(52) "/**
     * @Below is the Size of HR String
     */"
string(56) "/**
     * @Below is the Size of Coding String
     */"
string(59) "/**
     * @Below is the Size of Marketing String
     */"

```

**引用：**[https://www.php.net/manual/en/reflectionproperty.getdoccomment.php](https://www.php.net/manual/en/reflectionproperty.getdoccomment.php)