# PHP | ArrayObject count()函数

> 原文:[https://www . geesforgeks . org/PHP-arrayobject-count-function/](https://www.geeksforgeeks.org/php-arrayobject-count-function/)

**ArrayObject::count()函数**是 PHP 中的一个内置函数，用来获取 ArrayObject 中公共属性的个数。

**语法:**

```php
*int* ArrayObject::count( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数返回 ArrayObject 中公共属性的个数。

下面的程序说明了 PHP 中的 ArrayObject::count()函数:

**程序 1:**

```php
<?php 
// PHP program to illustrate the 
// ArrayObject::count() function 

// Declare an array and convert it
// into array object
$arrObject = new ArrayObject(
    array('Geeks', 'for', 'Geeks')
); 

// Use ArrayObject::count() function
// to count the number of public
// properties in the ArrayObject
$count = $arrObject->count(); 

print_r($count); 

?> 
```

**输出:**

```php
3

```

**程序二:**

```php
<?php 
// PHP program to illustrate the 
// ArrayObject::count() function 

// Declare an associative array
$arr = array(
    "a" => "Welcome",
    "b" => "to", 
    "c" => "GeeksforGeeks"
); 

// Create into array object 
$arrObject = new ArrayObject($arr); 

// Use ArrayObject::count() function
// to count the number of public
// properties in the ArrayObject
$count = $arrObject->count(); 

print_r($count); 

?> 
```

**输出:**

```php
3

```

**参考:**T2】https://www.php.net/manual/en/arrayobject.count.php