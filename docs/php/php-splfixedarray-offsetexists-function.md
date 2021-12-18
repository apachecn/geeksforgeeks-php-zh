# PHP|SplFixedArray offsetExists()函数

> Original: [https://www.geeksforgeeks.org/php-splfixedarray-offsetexists-function/](https://www.geeksforgeeks.org/php-splfixedarray-offsetexists-function/)

**SplFixedArray：：offsetExists()**函数是 PHP 中的内置函数，用于检查数组中是否存在所提供的索引。

**语法：**

```
*bool* SplFixedArray::offsetExists( $index )
```

**参数：**此函数接受指定所请求索引的单个参数**$index**。

**返回值：**如果找到请求的索引，则此函数返回 TRUE，否则返回 FALSE。

下面的程序演示了 PHP 中的**SplFixedArray：：offsetExists()**函数：

**程序 1：**

```
<?php

// Create a fixed size array
$gfg = new SplFixedArray(6);

$gfg[0] = 1;
$gfg[1] = 5;
$gfg[2] = 10;

// Check whether index exist or not
var_dump($gfg->offsetExists(2));
?>
```

**输出：**

```
bool(true)

```

**程序 2：**

```
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

// Iterate array and print values
while($i < 8) {

    // Check whether index exist or not
    var_dump($gfg->offsetExists($i)); 

    $i++;
}
?>
```

**输出：**

```
bool(true)
bool(true)
bool(true)
bool(true)
bool(true)
bool(true)
bool(false)
bool(false)

```

**引用：**[https://www.php.net/manual/en/splfixedarray.offsetexists.php](https://www.php.net/manual/en/splfixedarray.offsetexists.php)