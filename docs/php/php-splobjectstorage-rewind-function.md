# PHP|SplObjectStorage rewind()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-rewind-function/](https://www.geeksforgeeks.org/php-splobjectstorage-rewind-function/)

**SplObjectStorage：：Rewind()**函数是 PHP 中的一个内置函数，用于将迭代器倒回到第一个存储元素。

**语法：**

```
*void* SplObjectStorage::rewind()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的 S**plObjectStorage：：Rewind()**函数：

**程序 1：**

```
<?php

// Create an empty SplObjectStorage
$str = new SplObjectStorage();

$obj = new StdClass;
$obj2 = new StdClass;
$obj3 = new StdClass;

$str->attach($obj, "GFG");
$str->attach($obj2, "Geeks");
$str->attach($obj3, "FORK JAVA");

// Using rewind function
$str->rewind();

// Get current data 
var_dump($str->getInfo());

// Move on to next object
$str->next();

// Get current data 
var_dump($str->getInfo());

// Again using rewind function
$str->rewind();

// Get current data 
var_dump($str->getInfo());
?>
```

**输出：**

```
string(3) "GFG"
string(5) "Geeks"
string(3) "GFG"

```

**程序 2：**

```
<?php

$obj1 = new StdClass;
$obj2 = new StdClass;
$obj3 = new StdClass;

$gfg = new SplObjectStorage();
$gfg[$obj1] = "GFG";
$gfg[$obj2] = "GeeksClasses";
$gfg[$obj3] = "SUDO";

// Using rewind function
$gfg->rewind();

while($gfg->valid()) {
    var_dump($gfg->getInfo());

    // Moving to next element
    $gfg->next();
}
?>
```

**输出：**

```
string(3) "GFG"
string(12) "GeeksClasses"
string(4) "SUDO"

```

**引用：**[https://www.php.net/manual/en/splobjectstorage.rewind.php](https://www.php.net/manual/en/splobjectstorage.rewind.php)