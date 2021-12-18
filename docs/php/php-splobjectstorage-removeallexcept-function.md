# PHP|SplObjectStorage removeAllExcept()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-removeallexcept-function/](https://www.geeksforgeeks.org/php-splobjectstorage-removeallexcept-function/)

**SplObjectStorage：：removeAllExcept()**函数是 PHP 中的一个内置函数，用于从存储中删除除其他存储包含的对象之外的所有对象。

**语法：**

```php
*int* SplObjectStorage::removeAllExcept()
```

**参数：**此函数接受指定要保留对象存储的单个参数**$obj**。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的**SplObjectStorage：：removeAllExcept()**函数：

**程序 1：**

```php
<?php

$obj1 = new StdClass;
$obj2 = new StdClass;
$obj3 = new StdClass;

$gfg1 = new SplObjectStorage();
$gfg1[$obj1] = "Geeks";

$gfg2 = new SplObjectStorage();
$gfg2[$obj1] = "GFG";
$gfg2[$obj2] = "GeeksClasses";
$gfg2[$obj3] = "SUDO";

// Count all existing objects
var_dump(count($gfg2));

// Remove all objects of $gfg2 from $gfg2
$gfg2->removeAllExcept($gfg1);

// Print result after removeAll
var_dump(count($gfg2));
?>
```

**输出：**

```php
int(3)
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
$gfg2->removeAllExcept($gfg1);

// Print result  
var_dump(count($gfg2));

// Result remains same
$gfg2->removeAllExcept($gfg2);

// Print result  
var_dump(count($gfg2));

?>
```

**输出：**

```php
int(2)
int(1)
int(1)

```

**引用：**[https://www.php.net/manual/en/splobjectstorage.removeallexcept.php](https://www.php.net/manual/en/splobjectstorage.removeallexcept.php)