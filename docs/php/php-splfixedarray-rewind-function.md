# PHP|SplFixedArray Rewind()函数

> Original: [https://www.geeksforgeeks.org/php-splfixedarray-rewind-function/](https://www.geeksforgeeks.org/php-splfixedarray-rewind-function/)

**SplFixedArray：：Rewind()**函数是 PHP 中的一个内置函数，用于将数组迭代器倒回到起始位置。

**语法：**

```php
*void* SplFixedArray::rewind()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的**SplFixedArray：：Rewind()**函数：

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

// Print result before rewind
echo $gfg->current(). "\n";

// Using rewind function
$gfg->rewind();

// Print result after rewind
echo $gfg->current(). "\n";

?>
```

**输出：**

```php
10
1

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

// Iterate array and print values
while($i < 6) {

     // Using rewind function
     // it will rewind each time at initial index
     $gfg->rewind();

    // Print current value of index of the array
    echo $gfg->current(). "\n";

    // Move next each time of iteration
    $gfg->next();
    $i++;
}

?>
```

**输出：**

```php
1
1
1
1
1
1

```

**引用：**[https://www.php.net/manual/en/splfixedarray.rewind.php](https://www.php.net/manual/en/splfixedarray.rewind.php)