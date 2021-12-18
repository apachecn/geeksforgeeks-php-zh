# PHP | ArrayObject unserialize()函数

> 原文:[https://www . geeksforgeeks . org/PHP-arrayobject-unserialize-function/](https://www.geeksforgeeks.org/php-arrayobject-unserialize-function/)

**ArrayObject::unserialize()函数**是 PHP 中的一个内置函数，用于对序列化后的 ArrayObject 进行非序列化。

**语法:**

```
*void* ArrayObject::unserialize( *string* $serialized )
```

**参数:**该函数接受保存序列化数组对象的单个参数**$序列化**。

**返回值:**该函数返回未序列化的数组对象。

下面的程序说明了 PHP 中的 ArrayoObject::unserialize()函数:

**程序:**

```
<?php 
// PHP program to illustrate the 
// ArrayObject::unserialize() function 

// Declare an associative array
$arr = array(
    "a" => "Welcome",
    "b" => "to", 
    "c" => "GeeksforGeeks"
); 

// Create array object 
$arrObject = new ArrayObject($arr); 

// Use ArrayObject::serialize() function
$serialize1 = serialize($arrObject);

// Use ArrayObject::unserialize() function
$serialize2 = unserialize($serialize1);

// Display the result
var_dump($serialize1); 
var_dump($serialize2); 

?>
```

**输出:**

```
string(113) "C:11:"ArrayObject":89:{
    x:i:0;a:3:{
        s:1:"a";s:7:"Welcome";
        s:1:"b";s:2:"to";
        s:1:"c";s:13:"GeeksforGeeks";
    }
    ;m:a:0:{}
}"
object(ArrayObject)#2 (1) {
  ["storage":"ArrayObject":private]=>
  array(3) {
    ["a"]=>
    string(7) "Welcome"
    ["b"]=>
    string(2) "to"
    ["c"]=>
    string(13) "GeeksforGeeks"
  }
}

```

**参考:**T2】https://www.php.net/manual/en/arrayobject.unserialize.php