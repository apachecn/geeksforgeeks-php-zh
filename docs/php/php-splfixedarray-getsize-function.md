# PHP|SplFixedArray getSize()函数

> Original: [https://www.geeksforgeeks.org/php-splfixedarray-getsize-function/](https://www.geeksforgeeks.org/php-splfixedarray-getsize-function/)

**SplFixedArray：：getSize()**函数是 PHP 中的内置函数，用于获取数组的大小。

**语法：**

```php
*int* SplFixedArray::getSize()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回数组的大小。

下面的程序演示了 PHP 中的**SplFixedArray：：getSize()**函数：

**程序 1：**

```php
<?php

// Create a fixed array
$gfg = new SplFixedArray(15);

// Print Size of the array
echo $gfg->getSize();

?>
```

**输出：**

```php
15

```

**程序 2：**

```php
<?php

// Create some fixed size array
$gfg1 = new SplFixedArray(0);
$gfg2 = new SplFixedArray(9);
$gfg3 = new SplFixedArray(100);
$gfg4 = new SplFixedArray(878);

// Print Size of the array
echo $gfg1->getSize() . "\n";
echo $gfg2->getSize() . "\n";
echo $gfg3->getSize() . "\n";
echo $gfg4->getSize() . "\n";

// Set array size
$gfg1->setSize(100);
$gfg2->setSize(200);

// Print size after set
echo $gfg1->getSize() . "\n";
echo $gfg2->getSize() . "\n";
?>
```

**输出：**

```php
0
9
100
878
100
200

```

**引用：**[https://www.php.net/manual/en/splfixedarray.getsize.php](https://www.php.net/manual/en/splfixedarray.getsize.php)