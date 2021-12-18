# PHP|ds\Pair Clear()函数

> Original: [https://www.geeksforgeeks.org/php-dspair-clear-function/](https://www.geeksforgeeks.org/php-dspair-clear-function/)

**Ds\Pair：：Clear()函数**是 PHP 中的一个内置函数，用于从对中删除所有值。

**语法：**

```
*void* Ds\Pair::clear( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的 Ds\Pair：：Clear()函数：

**程序：**

```
<?php 

// Create new pair 
$pair = new \Ds\Pair("G", "GeeksforGeeks"); 

echo ("Original pair elements:\n"); 

// Display the pair elements 
print_r($pair); 

echo("Modified pair\n"); 

// Use clear() function to 
// remove pair elements 
$pair->clear(); 

// Display pair elements 
print_r($pair); 

?> 
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/ds-pair.clear.php](https://www.php.net/manual/en/ds-pair.clear.php)