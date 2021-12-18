# PHP|SplObjectStorage Valid()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-valid-function/](https://www.geeksforgeeks.org/php-splobjectstorage-valid-function/)

**SplObjectStorage：：Valid()**函数是 PHP 中的一个内置函数，用于检查当前存储条目是否有效。

**语法：**

```
*bool* SplObjectStorage::valid()
```

**参数：**此函数不接受任何参数。

**返回值：**如果迭代器条目有效，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明了 PHP 中的**SplObjectStorage：：Valid()**函数：

**程序 1：**

```
<?php

// Create an empty SplObjectStorage
$str = new SplObjectStorage();

$obj = new StdClass;
$obj2 = new StdClass;
$obj3 = new StdClass;

// Use attach() function to
// add object
$str->attach($obj, "GFG");

// Use rewind() function to rewind the 
// iterator to the first storage element
$str->rewind();

// Use valid() function to check current
// iterator is valid entry or not
print($str->valid());

?>
```

**输出：**

```
1

```

**程序 2：**

```
<?php

// Create an empty SplObjectStorage
$gfg = new SplObjectStorage();

$obj1 = new StdClass;
$obj2 = new StdClass;
$obj3 = new StdClass;

$gfg[$obj1] = "GFG";
$gfg[$obj2] = "GeeksClasses";
$gfg[$obj3] = "SUDO";

// Use rewind function
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

**引用：**[https://www.php.net/manual/en/splobjectstorage.valid.php](https://www.php.net/manual/en/splobjectstorage.valid.php)