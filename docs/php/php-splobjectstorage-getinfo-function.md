# PHP|SplObjectStorage getinfo()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-getinfo-function/](https://www.geeksforgeeks.org/php-splobjectstorage-getinfo-function/)

**SplObjectStorage：：getinfo()**函数是 PHP 中的一个内置函数，用于通过当前迭代器位置获取与对象关联的数据。

**语法：**

```
*mixed* SplObjectStorage::getinfo()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回与当前迭代器位置关联的对象。

以下程序说明了 PHP 中的**SplObjectStorage：：getinfo()**函数：

**程序 1：**

```
<?php

// Create New Empty Storage Class
$str = new SplObjectStorage();

$obj1 = new StdClass;

$str->attach($obj1, "GeksforGeeks");

$str->rewind();

$object = $str->current(); 

// Get info into $data 
$data   = $str->getInfo();

// Print Result
var_dump($object);
var_dump($data);

?>
```

**输出：**

```
object(stdClass)#2 (0) {
}
string(12) "GeksforGeeks"

```

**程序 2：**

```
<?php
// Create an Empty SplObjectStorage
$str = new SplObjectStorage();

$obj1 = new StdClass;
$obj2 = new StdClass;
$obj3 = new StdClass;
$obj4 = new StdClass;

$str->attach($obj1, "GeksforGeeks");
$str->attach($obj2, "GFG");
$str->attach($obj3);
$str->attach($obj4, "DSA");

$str->rewind();

// Iterate and print data on each index
while($str->valid()) {
    $index  = $str->key();
    $object = $str->current(); 
    $data   = $str->getInfo();

    var_dump($object);
    var_dump($data);
    $str->next();
}
?>
```

**输出：**

```
object(stdClass)#2 (0) {
}
string(12) "GeksforGeeks"
object(stdClass)#3 (0) {
}
string(3) "GFG"
object(stdClass)#4 (0) {
}
NULL
object(stdClass)#5 (0) {
}
string(3) "DSA"

```

**引用：**[https://www.php.net/manual/en/splobjectstorage.getinfo.php](https://www.php.net/manual/en/splobjectstorage.getinfo.php)