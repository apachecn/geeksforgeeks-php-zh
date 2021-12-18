# PHP|SplObjectStorage Attach()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-attach-function/](https://www.geeksforgeeks.org/php-splobjectstorage-attach-function/)

**SplObjectStorage：：Attach()**函数是 PHP 中的一个内置函数，用于将对象添加到 SplObjectStorage 中。

**语法：**

```
*void* SplObjectStorage::attach($obj, $val)
```

**参数：**此函数接受上述和下面描述的两个参数。

*   **$obj:** this is a required parameter to specify the object of the storage class.
*   **$val:** this is an optional parameter that specifies the value to add.

**返回值：**此函数不返回任何值。

以下程序说明了 PHP 中的**SplObjectStorage：：Attach()**函数：

**程序 1：**

```
<?php

// Declare new object
$obj = new StdClass;

// Create an empty storage class
$str = new SplObjectStorage();

// Attach $obj with String "GeeksforGeeks"
$str->attach($obj, "GeeksforGeeks");

// Print Result 
var_dump($str[$obj]);

?>
```

**输出：**

```
string(13) "GeeksforGeeks"

```

**程序 2：**

```
<?php

// Creating std classes
$obj1 = new StdClass;
$obj2 = new StdClass;
$obj3 = new StdClass;
$obj4 = new StdClass;

$str = new SplObjectStorage();
$str->attach($obj1);
$str->attach($obj2, "GFG");

// Another way to use attach() function
$str[$obj3] = "GeeksforGeeks";
$str[$obj4] = NULL ;

// Print Result
var_dump($str[$obj1]);
var_dump($str[$obj2]);
var_dump($str[$obj3]);
var_dump($str[$obj4]);

?>
```

**输出：**

```
NULL
string(3) "GFG"
string(13) "GeeksforGeeks"
NULL

```

**引用：**[https://www.php.net/manual/en/splobjectstorage.attach.php](https://www.php.net/manual/en/splobjectstorage.attach.php)