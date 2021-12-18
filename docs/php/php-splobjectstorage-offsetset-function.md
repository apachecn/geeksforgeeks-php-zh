# PHP|SplObjectStorage offsetSet()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-offsetset-function/](https://www.geeksforgeeks.org/php-splobjectstorage-offsetset-function/)

**SplObjectStorage：：offsetSet()**函数是 PHP 中的内置函数，用于设置存储对象。

**语法：**

```php
*void* SplObjectStorage::offsetSet($obj, $val)
```

**参数：**此函数接受上述和下面描述的两个参数：

*   **$obj:** it specifies the object to attach.
*   **$val:** it specifies the value to associate with the object.

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的**SplObjectStorage：：offsetSet()**函数：

**程序 1：**

```php
<?php

// Create an empty SplObjectStorage
$str = new SplObjectStorage;
$obj = new StdClass;

// Set offset $obj to $str 
$str->offsetSet($obj, "GeeksforGeeks");

// Print Result
var_dump($str->offsetGet($obj)); 
?>
```

**输出：**

```php
string(13) "GeeksforGeeks"

```

**程序 2：**

```php
<?php

// Create an Empty SplObjectStorage
$str = new SplObjectStorage();

$obj1 = new StdClass;
$obj2 = new StdClass;
$obj3 = new StdClass;
$obj4 = new StdClass;

// Attach objects
$str->offsetSet($obj1, "GeksforGeeks");
$str->offsetSet($obj2, "GFG");
$str->offsetSet($obj3);
$str->offsetSet($obj4, "Hello GFG");

// Print result
var_dump($str->offsetGet($obj1)); 
var_dump($str->offsetGet($obj2)); 
var_dump($str->offsetGet($obj4)); 
var_dump($str->offsetGet($obj3)); 

?>
```

**输出：**

```php
string(12) "GeksforGeeks"
string(3) "GFG"
string(9) "Hello GFG"
NULL

```

**引用：**[https://www.php.net/manual/en/splobjectstorage.offsetset.php](https://www.php.net/manual/en/splobjectstorage.offsetset.php)