# PHP|SplObjectStorage offsetUnset()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-offsetunset-function/](https://www.geeksforgeeks.org/php-splobjectstorage-offsetunset-function/)

**SplObjectStorage：：offsetUnset()**函数是 PHP 中的内置函数，用于设置存储中的对象。

**语法：**

```
*void* SplObjectStorage::offsetUnset( $object )
```

**参数：**此函数接受单个参数**$object**，该参数指定要取消设置的。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的**SplObjectStorage：：offsetUnset()**函数：

**程序 1：**

```
<?php

// Create an empty SplObjectStorage
$str = new SplObjectStorage;
$obj = new StdClass;

// Set offset $obj to $str 
$str->attach($obj, "GeeksforGeeks");

// Print Result before
var_dump(count($str));

// Unset object from storage
$str->offsetUnset($obj);

// Print Result after
var_dump(count($str));

?>
```

**输出：**

```
int(1)
int(0)

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

// Print Result before
var_dump(count($str));

// Unset object from storage
$str->offsetUnset($obj1);
$str->offsetUnset($obj2);
$str->offsetUnset($obj3);
$str->offsetUnset($obj4);

// Print Result after
var_dump(count($str));
?>
```

**输出：**

```
int(4)
int(0)

```

**引用：**[https://www.php.net/manual/en/splobjectstorage.offsetunset.php](https://www.php.net/manual/en/splobjectstorage.offsetunset.php)