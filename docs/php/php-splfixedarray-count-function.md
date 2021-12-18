# PHP|SplFixedArray count()函数

> Original: [https://www.geeksforgeeks.org/php-splfixedarray-count-function/](https://www.geeksforgeeks.org/php-splfixedarray-count-function/)

**SplFixedArray：：Count()**函数是 PHP 中的内置函数，用于返回数组的大小。

**语法：**

```php
*int* SplFixedArray::count()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回数组的大小。

以下程序说明了 PHP 中的**SplFixedArray：：Count()**函数：

**程序 1：**

```php
<?php

// Create an array of fixed size 10
$array = new SplFixedArray(10);

// Print size of the array
echo $array->count();
?>
```

**输出：**

```php
10

```

**程序 2：**

```php
<?php

// Creating fixed size array
$gfg = new SplFixedArray(8);
$gfg1 = new SplFixedArray(7);
$gfg2 = new SplFixedArray(9);
$gfg3 = new SplFixedArray(100);
$gfg4 = new SplFixedArray(878);
$gfg5 = new SplFixedArray(0);

// Print size of the array
echo $gfg1->count(). "\n";
echo $gfg2->count(). "\n";
echo $gfg3->count(). "\n";
echo $gfg4->count(). "\n";

// Count function can be used
// via passing parameters
echo count($gfg5) . "\n";
echo count($gfg) . "\n";
?>
```

**输出：**

```php
7
9
100
878
0
8

```

**引用：**[https://www.php.net/manual/en/splfixedarray.count.php](https://www.php.net/manual/en/splfixedarray.count.php)