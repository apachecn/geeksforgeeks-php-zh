# PHP | ArrayIterator unserialize()函数

> 原文:[https://www . geeksforgeeks . org/PHP-arrayiterator-unserialize-function/](https://www.geeksforgeeks.org/php-arrayiterator-unserialize-function/)

**ArrayIterator::unserialize()函数**是 PHP 中的一个内置函数，用于对序列化对象进行非序列化。

**语法:**

```
*void* ArrayIterator::unserialize( *string* $serialized )
```

**参数:**这个函数接受单个参数**$序列化的**，它保存序列化数组迭代器对象。

**返回值:**该函数返回未序列化对象的序列化数组运算符对象。

下面的程序说明了 PHP 中的 ArrayIterator::unserialize()函数:

**程序 1:**

```
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array('G', 'e', 'e', 'k', 's')
);

// Serialize the element
$serialize = serialize($arrItr); 

// Display the output
var_dump($serialize);

// Unserialize the serialize element
$unserialize = unserialize($serialize);

// Display the result
var_dump($unserialize);

?>
```

**输出:**

```
string(107) "C:13:"ArrayIterator":81:{x:i:0;a:5:{i:0;s:1:"G";i:1;
s:1:"e";i:2;s:1:"e";i:3;s:1:"k";i:4;s:1:"s";};m:a:0:{}}"
object(ArrayIterator)#2 (1) {
  ["storage":"ArrayIterator":private]=>
  array(5) {
    [0]=>
    string(1) "G"
    [1]=>
    string(1) "e"
    [2]=>
    string(1) "e"
    [3]=>
    string(1) "k"
    [4]=>
    string(1) "s"
  }
}

```

**程序二:**

```
<?php

// Declare an ArrayIterator
$arrItr = new ArrayIterator(
    array(
        "a" => "Geeks",
        "b" => "for",
        "c" => "Geeks"
    )
);

// Append some elements
$arrItr->append("Computer"); 
$arrItr->append("Science"); 
$arrItr->append("Portal"); 

// Serialize the element
$serialize = serialize($arrItr); 

// Display the output
var_dump($serialize);

// Unserialize the element
$unserialize = unserialize($serialize); 

// Display the output
var_dump($unserialize);

?>
```

**输出:**

```
string(160) "C:13:"ArrayIterator":133:{x:i:0;a:6:{s:1:"a";s:5:"Geeks";
s:1:"b";s:3:"for";s:1:"c";s:5:"Geeks";i:0;s:8:"Computer";i:1;
s:7:"Science";i:2;s:6:"Portal";};m:a:0:{}}"
object(ArrayIterator)#2 (1) {
  ["storage":"ArrayIterator":private]=>
  array(6) {
    ["a"]=>
    string(5) "Geeks"
    ["b"]=>
    string(3) "for"
    ["c"]=>
    string(5) "Geeks"
    [0]=>
    string(8) "Computer"
    [1]=>
    string(7) "Science"
    [2]=>
    string(6) "Portal"
  }
}

```

**参考:**T2】https://www.php.net/manual/en/arrayiterator.unserialize.php