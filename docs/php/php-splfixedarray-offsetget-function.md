# PHP|SplFixedArray offsetGet()函数

> Original: [https://www.geeksforgeeks.org/php-splfixedarray-offsetget-function/](https://www.geeksforgeeks.org/php-splfixedarray-offsetget-function/)

**SplFixedArray：：offsetGet()**函数是 PHP 中的内置函数，用于获取数组中指定索引的偏移量。

**语法：**

```
*mixed* SplFixedArray::offsetGet( $index )
```

**参数：**此函数接受指定请求偏移量的单个参数**$index**。

**返回值：**此函数返回数组的偏移量。
以下程序说明 PHP：
**程序 1：**中的**SplFixedArray：：OffsetGet()**函数

## PHP

```
<?php

// Create a fixed size array
$gfg = new SplFixedArray(6);

$gfg[0] = 1;
$gfg[1] = 5;
$gfg[2] = 10;

// Check whether index exist or not
var_dump($gfg->offsetGet(2));
?>
```

**Output:** 

```
int(10)
```