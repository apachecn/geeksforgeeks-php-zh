# PHP|SplObjectStorage count()函数

> Original: [https://www.geeksforgeeks.org/php-splobjectstorage-count-function/](https://www.geeksforgeeks.org/php-splobjectstorage-count-function/)

**SplObjectStorage：：Count()**函数是 PHP 中的一个内置函数，用于计算存储中的对象数量。

**语法：**

```
*int* SplObjectStorage::count()
```

**参数：**此函数不包含任何参数。

**返回值：**此函数返回存储中的对象数。

以下程序说明了 PHP 中的**SplObjectStorage：：Count()**函数：

**程序 1：**

```
<?php

// Declare Empty SplObjectStorage
$gfg = new SplObjectStorage();
$gfg1 = new StdClass;
$gfg2 = new StdClass;
$gfg3 = new StdClass;

// Add object to SplObjectStorage class
$gfg->attach($gfg1);
$gfg->attach($gfg2);
$gfg->attach($gfg3);

// Use count() function to count object
var_dump($gfg->count());
?>
```

**输出：**

```
int(3)

```

**程序 2：**

```
<?php

// Declare Empty SplObjectStorage
$gfg = new SplObjectStorage();
$gfg1 = new StdClass;
$gfg2 = new StdClass;
$gfg3 = new StdClass;

// Add object to SplObjectStorage class
$gfg->attach($gfg1);
$gfg->attach($gfg2);
$gfg->attach($gfg3);

// Use count in different way
// Passing object as parameter
var_dump(count($gfg));
?>
```

**输出：**

```
int(3)

```

**引用：**[https://www.php.net/manual/en/splobjectstorage.count.php](https://www.php.net/manual/en/splobjectstorage.count.php)