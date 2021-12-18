# PHP|SplObjectStorage setInfo()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-setinfo-function/](https://www.geeksforgeeks.org/php-splobjectstorage-setinfo-function/)

**SplObjectStorage：：setInfo()**函数是 PHP 中的一个内置函数，用于设置与当前迭代器条目相关联的数据。

**语法：**

```
*void* SplObjectStorage::setInfo( $val )
```

**参数：**此函数接受单个参数**$val**，该参数指定要与存储的当前迭代器条目相关联的数据。

**返回值：**此函数不返回任何值。

以下程序说明了 PHP 中的**SplObjectStorage：：setInfo()**函数：

**程序 1：**

```
<?php

$str = new SplObjectStorage();

$obj1 = new StdClass;

$str->attach($obj1, "GeeksforGeeks");

$str->rewind();

// Set new info for $obj1 in storage $str
$str->setInfo("new_GeeksforGeeks");

// Print Result
var_dump($str[$obj1]);
?>
```

**输出：**

```
string(17) "new_GeeksforGeeks"

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

    $gfg->setInfo("Modified_GFG_DATA");
    var_dump($gfg->getInfo());

    // Moving to next element
    $gfg->next();
}
?>
```

**输出：**

```
string(17) "Modified_GFG_DATA"
string(17) "Modified_GFG_DATA"
string(17) "Modified_GFG_DATA"

```

**引用：**[https://www.php.net/manual/en/splobjectstorage.setinfo.php](https://www.php.net/manual/en/splobjectstorage.setinfo.php)