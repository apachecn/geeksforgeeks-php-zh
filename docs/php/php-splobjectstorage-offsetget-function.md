# PHP|SplObjectStorage offsetGet()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-offsetget-function/](https://www.geeksforgeeks.org/php-splobjectstorage-offsetget-function/)

**SplObjectStorage：：offsetGet()**函数是 PHP 中的一个内置函数，用于获取与对象相关的数据。
**语法：**和

```php
*object* SplObjectStorage::offsetGet($obj)
```

**参数：**此函数接受指定要获取的对象的单个参数**$obj**。
**返回值：**此函数返回以前与存储中的对象关联的数据。
下面的程序说明 PHP：
**程序 1：**和
中的**SplObjectStorage：：OffsetGet()**函数

## PHP

```php
<?php

// Create an empty SplObjectStorage
$str = new SplObjectStorage;
$obj = new StdClass;

// Attach $obj to $str
$str->attach($obj, "GeeksforGeeks");

// Print Result
var_dump($str->offsetGet($obj));
?>
```

**Output:** 

```php
string(13) "GeeksforGeeks"
```

**程序 2：**和

## PHP

```php
<?php

// Create an Empty SplObjectStorage
$str = new SplObjectStorage();

$obj1 = new StdClass;
$obj2 = new StdClass;
$obj3 = new StdClass;
$obj4 = new StdClass;

// Attach objects
$str->attach($obj1, "GeksforGeeks");
$str->attach($obj2, "GFG");
$str->attach($obj3);
$str->attach($obj4, "Hello GFG");

// Print result
var_dump($str->offsetGet($obj1));
var_dump($str->offsetGet($obj2));
var_dump($str->offsetGet($obj4));
var_dump($str->offsetGet($obj3));

?>
```

**Output:** 

```php
string(12) "GeksforGeeks"
string(3) "GFG"
string(9) "Hello GFG"
NULL
```

**引用：**[https://www.php.net/manual/en/splobjectstorage.offsetget.php](https://www.php.net/manual/en/splobjectstorage.offsetget.php)