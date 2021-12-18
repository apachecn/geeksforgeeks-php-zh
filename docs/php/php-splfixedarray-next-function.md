# PHP|SplFixedArray Next()函数

> Original: [https://www.geeksforgeeks.org/php-splfixedarray-next-function/](https://www.geeksforgeeks.org/php-splfixedarray-next-function/)

**SplFixedArray：：Next()**函数是 PHP 中的一个内置函数，用于将数组元素移动到数组的下一个条目。

**语法：**

```php
*void* SplFixedArray::next()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

以下程序说明了 PHP 中的**SplFixedArray：：Next()**函数：

**程序 1：**

```php
<?php

// Create a fixed size array
$gfg = new SplFixedArray(6);

$gfg[0] = 1;
$gfg[1] = 5;
$gfg[2] = 10;

// Move to next index
$gfg->next();
$gfg->next();

// Print the value of current index
echo $gfg->current() . "\n";
?>
```

**输出：**

```php
10

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

    // Print current value of index of the array
    echo $gfg->current(). "\n";

    // Move next each time of iteration
    $gfg->next();
}
?>
```

**输出：**

```php
1
5
1
11
15
17

```

**引用：**[https://www.php.net/manual/en/splfixedarray.next.php](https://www.php.net/manual/en/splfixedarray.next.php)