# PHP|SplObjectStorage removeAll()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-removeall-function/](https://www.geeksforgeeks.org/php-splobjectstorage-removeall-function/)

**SplObjectStorage：：removeAll()**函数是 PHP 中的一个内置函数，用于从当前存储中删除另一个存储中包含的所有对象。

**语法：**

```php
*void* SplObjectStorage::removeAll( $obj )
```

**参数：**此函数接受单个参数**$obj**，该参数指定要从当前存储中删除的存储。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的**SplObjectStorage：：removeAll()**函数：

**程序 1：**

```php
<?php

$obj1 = new StdClass;
$obj2 = new StdClass;

$gfg1 = new SplObjectStorage();
$gfg1[$obj1] = "Geeks";

$gfg2 = new SplObjectStorage();
$gfg2[$obj1] = "GFG";
$gfg2[$obj2] = "GeeksClasses";

// Count and print all existing objects
var_dump(count($gfg2));

// Remove all objects of $gfg1 from $gfg2
$gfg2->removeAll($gfg1);

// Print result after removeAll
var_dump(count($gfg2));
?>
```

**输出：**

```php
int(2)
int(1)

```

**程序 2：**

```php
<?php

$obj1 = new StdClass;
$obj2 = new StdClass;

$gfg1 = new SplObjectStorage();
$gfg1[$obj1] = "Geeks";

$gfg2 = new SplObjectStorage();
$gfg2[$obj1] = "GFG";
$gfg2[$obj2] = "GeeksClasses";

// Count and print all existing objects
var_dump(count($gfg2));

// Remove all objects of $gfg1 from $gfg2
$gfg2->removeAll($gfg1);

// Print result after removeAll
var_dump(count($gfg2));

// Remove all objects itself $gfg2
$gfg2->removeAll($gfg2);

// Print result after removeAll
var_dump(count($gfg2));

?>
```

**输出：**

```php
int(2)
int(1)
int(0)

```

**引用：**[https://www.php.net/manual/en/splobjectstorage.removeall.php](https://www.php.net/manual/en/splobjectstorage.removeall.php)