# PHP|SplFixedArray offsetUnset()函数

> Original: [https://www.geeksforgeeks.org/php-splfixedarray-offsetunset-function/](https://www.geeksforgeeks.org/php-splfixedarray-offsetunset-function/)

**SplFixedArray：：offsetUnset()**函数是 PHP 中的内置函数，用于取消设置请求的索引值。

**语法：**

```php
*void* SplFixedArray::offsetUnset( $index )
```

**参数：**此函数接受单个参数**$index**，该参数指定需要取消设置其值的所需索引。

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的**SplFixedArray：：offsetUnset()**函数：

**程序 1：**

```php
<?php

// Create a fixed size array
$gfg = new SplFixedArray(6);

$gfg[0] = 1;
$gfg[1] = 5;
$gfg[2] = 10;

// Print current offset
var_dump($gfg->offsetGet(2));

// Unset offset
$gfg->offsetUnset (2);

// Print after unset
var_dump($gfg->offsetGet(2));

?>
```

**输出：**

```php
int(10)
NULL

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

$i = 0;

while($i < 6) {

    // Print current offset
    var_dump($gfg->offsetGet($i));

    // Unset offset
    $gfg->offsetUnset ($i);

    // Print after unset
    var_dump($gfg->offsetGet($i));

    $i++;
}
?>
```

**输出：**

```php
int(1)
NULL
int(5)
NULL
int(1)
NULL
int(11)
NULL
int(15)
NULL
int(17)
NULL

```

**引用：**[https://www.php.net/manual/en/splfixedarray.offsetunset.php](https://www.php.net/manual/en/splfixedarray.offsetunset.php)