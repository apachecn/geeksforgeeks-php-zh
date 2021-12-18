# PHP|SplObjectStorage key()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-key-function/](https://www.geeksforgeeks.org/php-splobjectstorage-key-function/)

**SplObjectStorage：：key()**函数是 PHP 中的一个内置函数，用于获取当前指向的迭代器的索引。

**语法：**

```php
*int* SplObjectStorage::key()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回迭代器当前指向的索引。

下面的程序说明了 PHP 中的**SplObjectStorage：：key()**函数：

**程序 1：**

```php
<?php

// Create an empty SplObjectStorage
$str = new SplObjectStorage();

$obj = new StdClass;

$str->attach($obj, "d1");

$str->rewind();

// Get current index 
$index  = $str->key();

// Print Result
var_dump($index);
?>
```

**输出：**

```php
int(0)

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

$str->attach($obj1, "GeksforGeeks");
$str->attach($obj2, "GFG");
$str->attach($obj3);
$str->attach($obj4, "DSA");

$str->rewind();

// Iterate and print data on each index
while($str->valid()) {

    // Get index 
    $index  = $str->key();
    $object = $str->current(); 
    $data   = $str->getInfo();

    var_dump($index, $data);
    $str->next();
}
?>
```

**输出：**

```php
int(0)
string(12) "GeksforGeeks"
int(1)
string(3) "GFG"
int(2)
NULL
int(3)
string(3) "DSA"

```

**引用：**[https://www.php.net/manual/en/splobjectstorage.key.php](https://www.php.net/manual/en/splobjectstorage.key.php)