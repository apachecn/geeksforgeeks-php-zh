# PHP | ArrayObject serialize()函数

> 原文:[https://www . geesforgeks . org/PHP-arrayobject-serialize-function/](https://www.geeksforgeeks.org/php-arrayobject-serialize-function/)

**ArrayObject::serialize()函数**是 PHP 中的一个内置函数，用于序列化 ArrayObject。

**语法:**

```php
*string* ArrayObject::serialize( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数返回数组对象的序列化表示。

下面的程序说明了 PHP 中的 ArrayObject::serialize()函数:

**程序:**

```php
<?php 
// PHP program to illustrate the 
// ArrayObject::serialize() function 

// Declare an associative array
$arr = array(
    "a" => "Welcome",
    "b" => "to", 
    "c" => "GeeksforGeeks"
); 

// Create array object 
$arrObject = new ArrayObject($arr); 

// Use ArrayObject::serialize() function
// to get the behavior of flags
$serialize1 = serialize($arrObject);
$serialize2 = $arrObject->serialize();

// Display the result
var_dump($serialize1); 
var_dump($serialize2); 

?> 
```

**输出:**

```php
string(113) "C:11:"ArrayObject":89:{
    x:i:0;a:3:{
        s:1:"a";s:7:"Welcome";
        s:1:"b";s:2:"to";
        s:1:"c";s:13:"GeeksforGeeks";
    }
    ;m:a:0:{}
}"
string(89) "x:i:0;a:3 {
    s:1:"a";s:7:"Welcome";
    s:1:"b";s:2:"to";
    s:1:"c";s:13:"GeeksforGeeks";
};m:a:0:{}"

```

**参考:**T2】https://www.php.net/manual/en/arrayobject.serialize.php