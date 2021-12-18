# PHP | ArrayObject getFlags()函数

> 原文:[https://www . geesforgeks . org/PHP-arrayobject-getflags-function/](https://www.geeksforgeeks.org/php-arrayobject-getflags-function/)

**ArrayObject::getFlags()函数**是 PHP 中的一个内置函数，用于获取 ArrayObject 的标志行为。

**语法:**

```
*int* ArrayObject::getFlags( *void* )
```

**参数:**此功能不接受任何参数。

**返回值:**该函数返回数组对象的行为标志。

下面的程序说明了 PHP 中的 ArrayObject::getFlags()函数:

**程序 1:**

```
<?php 
// PHP program to illustrate the 
// ArrayObject::getFlags() function 

// Declare an array and convert it into
// array object
$arrObject = new ArrayObject(
    array('Geeks', 'for', 'Geeks')
); 

// Use ArrayObject::getFlags() function
// to get the behavior of flags
$flag = $arrObject->getFlags(); 

var_dump($flag); 

// Set a new flags
$arrObject->setFlags(ArrayObject::ARRAY_AS_PROPS);

// Use ArrayObject::getFlags() function
// to get the behavior of flags
$flag = $arrObject->getFlags(); 

var_dump($flag); 

?> 
```

**输出:**

```
int(0)
int(2)

```

**程序二:**

```
<?php 
// PHP program to illustrate the 
// ArrayObject::getFlags() function 

// Declare an associative array
$arr = array(
    "a" => "Welcome",
    "b" => "to", 
    "c" => "GeeksforGeeks"
); 

// Create array object 
$arrObject = new ArrayObject($arr); 

// Use ArrayObject::getFlags() function
// to get the behavior of flags
$flag = $arrObject->getFlags(); 

var_dump($flag); 

// Set a new flags
$arrObject->setFlags(ArrayObject::STD_PROP_LIST);

// Use ArrayObject::getFlags() function
// to get the behavior of flags
$flag = $arrObject->getFlags(); 

var_dump($flag); 

?>
```

**输出:**

```
int(0)
int(1)

```

**参考:**T2】https://www.php.net/manual/en/arrayobject.getflags.php