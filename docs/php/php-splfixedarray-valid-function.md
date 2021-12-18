# PHP|SplFixedArray Valid()函数

> Original: [https://www.geeksforgeeks.org/php-splfixedarray-valid-function/](https://www.geeksforgeeks.org/php-splfixedarray-valid-function/)

**SplFixedArray：：Valid()**函数是 PHP 中的内置函数，用于检查数组是否可以包含更多元素。

**语法：**

```php
*bool* SplFixedArray::valid()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回 TRUE，否则返回 FALSE。

以下程序说明了 PHP 中的**SplFixedArray：：Valid()**函数：

**程序 1：**

```php
<?php

// Create a fixed size array
$gfg = new SplFixedArray(3);

// Move to two step forword
$gfg->next();
$gfg->next();

// Print result
var_dump($gfg->valid());

$gfg->next();

// Print result
var_dump($gfg->valid());

$gfg->next();

// Print result
var_dump($gfg->valid());
?>
```

**输出：**

```php
bool(true)
bool(false)
bool(false)

```

**程序 2：**

```php
<?php

// Create some fixed size array
$gfg = new SplFixedArray(6);

$gfg[0] = 1;
$gfg[1] = 5;
$gfg[2] = 1;
$gfg[4] = 15;
$gfg[5] = 22;

// Iterate array and print values
while($gfg->valid()) {

    // Print current value of index of the array
    var_dump($gfg->valid());

    // Move next each time of iteration
    $gfg->next();
}
?>
```

**输出：**

```php
bool(true)
bool(true)
bool(true)
bool(true)
bool(true)
bool(true)

```

**引用：**[https://www.php.net/manual/en/splfixedarray.valid.php](https://www.php.net/manual/en/splfixedarray.valid.php)