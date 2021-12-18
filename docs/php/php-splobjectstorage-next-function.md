# PHP|SplObjectStorage Next()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-next-function/](https://www.geeksforgeeks.org/php-splobjectstorage-next-function/)

**SplObjectStorage：：Next()**函数是 PHP 中的一个内置函数，用于移动到存储的下一个条目。

**语法：**

```php
*void* SplObjectStorage::next()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的**SplObjectStorage：：Next()**函数：

**程序 1：**

```php
<?php

// Create an empty SplObjectStorage
$str = new SplObjectStorage();

$obj = new StdClass;
$obj2 = new StdClass;

// Use attach() function to add object
$str->attach($obj, "GFG");
$str->attach($obj2, "Geeks");

$str->rewind();

// Get the current data 
var_dump($str->getInfo());

// Move on to next object
$str->next();

// Print result of next entry
var_dump($str->getInfo());
?>
```

**输出：**

```php
string(3) "GFG"
string(5) "Geeks"

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

// Use attach() function to add object
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

    // Moving each time next entry
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

**引用：**[https://www.php.net/manual/en/splobjectstorage.next.php](https://www.php.net/manual/en/splobjectstorage.next.php)