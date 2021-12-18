# PHP|SplFixedArray setSize()函数

> Original: [https://www.geeksforgeeks.org/php-splfixedarray-setsize-function/](https://www.geeksforgeeks.org/php-splfixedarray-setsize-function/)

**SplFixedArray：：setSize()**函数是 PHP 中的内置函数，用于设置数组的大小。

**语法：**

```php
*bool* SplFixedArray::setSize( $size )
```

**参数：**此函数接受指定数组大小的单个参数**$size**。

**返回值：**此函数成功时返回 TRUE，否则返回 FALSE。

下面的程序演示了 PHP 中的**SplFixedArray：：setSize()**函数：

**程序 1：**

```php
<?php

// Create fixed size array
$gfg = new SplFixedArray(50);

// Print size before set
echo $gfg->getSize() . "\n";

// Set size of array 
$gfg->setSize(110);

// Print result after set the size
echo $gfg->getSize() . "\n";
?>
```

**输出：**

```php
50
110

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

**引用：**[https://www.php.net/manual/en/splfixedarray.setsize.php](https://www.php.net/manual/en/splfixedarray.setsize.php)