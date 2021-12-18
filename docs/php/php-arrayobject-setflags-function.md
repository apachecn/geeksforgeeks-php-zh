# PHP | ArrayObject setFlags()函数

> 原文:[https://www . geesforgeks . org/PHP-arrayobject-set flags-function/](https://www.geeksforgeeks.org/php-arrayobject-setflags-function/)

**ArrayObject::setFlags()函数**是 PHP 中的一个内置函数，用来设置标志来改变 ArrayObject 的行为。

**语法:**

```
*void* ArrayObject::setFlags( *int* $flags )
```

**参数:**该函数接受单个参数 **$flags** ，该参数保存新数组对象的行为。此参数保存位掩码或命名常数。

**返回值:**该函数不返回值。

下面的程序说明了 PHP 中的 ArrayObject::setFlags()函数:

**程序 1:**

```
<?php 
// PHP program to illustrate the 
// ArrayObject::getFlags() function 

// Declare an array and convert
// it into array object
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

**参考:**T2】https://www.php.net/manual/en/arrayobject.setflags.php