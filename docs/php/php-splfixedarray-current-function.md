# PHP|SplFixedArray Current()函数

> Original: [https://www.geeksforgeeks.org/php-splfixedarray-current-function/](https://www.geeksforgeeks.org/php-splfixedarray-current-function/)

**SplFixedArray：：Current()**函数是 PHP 中的一个内置函数，用于获取数组的当前条目。

**语法：**

```
*mixed* SplFixedArray::current()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回数组的当前条目。

下面的程序演示了 PHP 中的**SplFixedArray：：Current()**函数：

**程序 1：**

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

$gfg->next();
echo $gfg->current(). "\n";
$gfg->rewind();
echo $gfg->current(). "\n";
?>
```

**输出：**

```
5
1

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

// Iterate array and print its values
while( $gfg->valid() ) {
    echo $gfg->current() . "\n";
    $gfg->next();
}
?>
```

**输出：**

```
1
5
1
11
15
17

```

**引用：**[https://www.php.net/manual/en/splfixedarray.current.php](https://www.php.net/manual/en/splfixedarray.current.php)