# PHP|SplFixedArray Key()函数

> Original: [https://www.geeksforgeeks.org/php-splfixedarray-key-function/](https://www.geeksforgeeks.org/php-splfixedarray-key-function/)

**SplFixedArray：：key()**函数是 PHP 中的一个内置函数，用于获取数组当前索引的键。

**语法：**

```php
*int* SplFixedArray::key()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回数组当前索引的键。

下面的程序演示了 PHP 中的**SplFixedArray：：key()**函数：

**程序 1：**

```php
<?php

// Create a fixed size array
$gfg = new SplFixedArray(6);

$gfg[0] = 1;
$gfg[1] = 5;
$gfg[2] = 1;

$gfg->next();
$gfg->next();

// Print key of current position
echo $gfg->key() . "\n";
?>
```

**输出：**

```php
2

```

**程序 2：**

```php
<?php

// Create some fixed size array
$gfg = new SplFixedArray(6);

$gfg[0] = 1;
$gfg[1] = 5;
$gfg[2] = 1;
$gfg[3] = 11;
$gfg[4] = 15;
$gfg[5] = 17;

// Iterate array and print values
while($gfg->valid()) {

    // Print Key of each Index
    echo $gfg->key(). "\n";
    $gfg->next();
}
?>
```

**输出：**

```php
0
1
2
3
4
5

```

**引用：**[https://www.php.net/manual/en/splfixedarray.key.php](https://www.php.net/manual/en/splfixedarray.key.php)