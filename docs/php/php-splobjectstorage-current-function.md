# PHP|SplObjectStorage Current()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-current-function/](https://www.geeksforgeeks.org/php-splobjectstorage-current-function/)

**SplObjectStorage：：Current()**函数是 PHP 中的一个内置函数，用于获取存储的当前条目。

**语法：**

```
*object* SplObjectStorage::current()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回当前存储的对象。

下面的程序说明了 PHP 中的**SplObjectStorage：：Current()**函数：

**程序 1：**

```
<?php

// Declare an SplObjectStorage
$storage = new SplObjectStorage();

// Declare new object
$obj = new StdClass;

// Use attach() function to add object
$storage->attach($obj, "GeeksforGeeks");

$storage->rewind();

// Use current() function to get
// the current object
$object = $storage->current(); 
$data = $storage->getInfo();

var_dump($object);
var_dump($data);
?>
```

**输出：**

```
object(stdClass)#2 (0) {
}
string(13) "GeeksforGeeks"

```

**程序 2：**

```
<?php

// Declare an SplObjectStorage
$str = new SplObjectStorage();

// Declare new object
$obj1 = new StdClass;
$obj2 = new StdClass;
$obj3 = new StdClass;
$obj4 = new StdClass;

// Use attach() function to add object
$str->attach($obj1, "GeeksforGeeks");
$str->attach($obj2, "GFG");
$str->attach($obj3, "Geeks");
$str->attach($obj4, "PHP");

$str->rewind();

while($str->valid()) {
    $index = $str->key();

    // Use current() function to get
    // the current object
    $object = current($str); 
    $data = $str->getInfo();

    var_dump($object);
    var_dump($data);
    $str->next();
}
?>
```

**输出：**

```
bool(false)
string(13) "GeeksforGeeks"
bool(false)
string(3) "GFG"
bool(false)
string(5) "Geeks"
bool(false)
string(3) "PHP"

```

**引用：**[https://www.php.net/manual/en/splobjectstorage.current.php](https://www.php.net/manual/en/splobjectstorage.current.php)