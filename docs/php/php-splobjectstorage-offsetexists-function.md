# PHP|SplObjectStorage offsetExists()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-offsetexists-function/](https://www.geeksforgeeks.org/php-splobjectstorage-offsetexists-function/)

**SplObjectStorage：：offsetExists()**函数是 PHP 中的内置函数，用于检查存储中是否存在对象。

**语法：**

```
*bool* SplObjectStorage::offsetExists($object)
```

**参数：**此函数接受指定要检查的对象的单个参数**$object**。
**返回值：**如果存储中存在对象，则此函数返回 TRUE，否则返回 FALSE。
下面的程序说明了 PHP 中的**SplObjectStorage：：offsetExists()**函数：

**程序 1：**

## PHP

```
<?php

// Create an empty SplObjectStorage
$str = new SplObjectStorage;
$obj = new StdClass;

// Attach $obj to $str
$str->attach($obj);

// Print Result
var_dump($str->offsetExists($obj));
?>
```

**Output:** 

```
bool(true)
```