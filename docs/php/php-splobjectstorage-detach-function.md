# PHP|SplObjectStorage Detach()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-detach-function/](https://www.geeksforgeeks.org/php-splobjectstorage-detach-function/)

**SplObjectStorage：：Detach()**函数是 PHP 中的一个内置函数，用于从存储中删除对象。

**语法：**

```
*void* SplObjectStorage::detach($obj)
```

**参数：**此函数接受单个参数**$obj**，该参数指定要从存储中删除的对象。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的**SplObjectStorage：：Detach()**函数：

**程序 1：**

```
<?php

// Creating class 
$obj = new StdClass;

// Create an empty storage class
$str = new SplObjectStorage();

// Add some object
$str->attach($obj, "GeeksforGeeks");

// Print result before detaching 
var_dump(count($str));

// Detaching object
$str->detach($obj);

// Print result after detach
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

// Creating class 
$obj1 = new StdClass;
$obj2 = new StdClass;
$obj3 = new StdClass;

// Create an empty storage class
$str = new SplObjectStorage();

// Add some object
$str->attach($obj1, "GeeksforGeeks");
$str->attach($obj2);
$str->attach($obj3, "GFG");

// Print result before detaching 
var_dump(count($str));

// Detaching object
$str->detach($obj1);

// Print result after detach first object
var_dump(count($str));

// Detaching object
$str->detach($obj3);

// Print result after detach second object
var_dump(count($str));
?>
```

**输出：**

```
int(3)
int(2)
int(1)

```

**引用：**[https://www.php.net/manual/en/splobjectstorage.detach.php](https://www.php.net/manual/en/splobjectstorage.detach.php)