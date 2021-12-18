# PHP|SplObjectStorage 包含()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-contains-function/](https://www.geeksforgeeks.org/php-splobjectstorage-contains-function/)

**SplObjectStorage：：CONTAINS()**函数是 PHP 中的一个内置函数，用于检查存储对象是否包含指定的对象。

**语法：**

```
*bool* SplObjectStorage::contains( $value )
```

**参数：**此函数接受单个参数**$value**，该参数指定要检查的存储对象。

**返回值：**如果存储对象包含指定对象，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明了 PHP 中的**SplObjectStorage：：CONTAINS()**函数：

**程序 1：**

```
<?php
$gfg1 = new StdClass;
$gfg2 = new StdClass;

// Declare Empty SplObjectStorage
$str = new SplObjectStorage();

$str[$gfg1] = "GeeksforGeeks";

// Print result
var_dump($str->contains($gfg1));
var_dump($str->contains($gfg2));

?>
```

**输出：**

```
bool(true)
bool(false)

```

**程序 2：**

```
<?php
$gfg1 = new StdClass;
$gfg2 = new StdClass;

// Declare Empty SplObjectStorage
$str = new SplObjectStorage();

$str[$gfg1] = "GeeksforGeeks";

// Print result
var_dump($str->contains($gfg1));
var_dump($str->contains($gfg2));

// detach and print result
$str->detach($gfg1);
var_dump($str->contains($gfg1));

?>
```

**输出：**

```
bool(true)
bool(false)
bool(false)

```

**引用：**[https://www.php.net/manual/en/splobjectstorage.contains.php](https://www.php.net/manual/en/splobjectstorage.contains.php)