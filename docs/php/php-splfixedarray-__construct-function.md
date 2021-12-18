# PHP|SplFixedArray__Construct()函数

> Original: [https://www.geeksforgeeks.org/php-splfixedarray-__construct-function/](https://www.geeksforgeeks.org/php-splfixedarray-__construct-function/)

SplFixedArray：：__Construct()函数是 PHP 中的内置函数，用于构造新的固定大小的数组。

**语法：**

```php
*void* SplFixedArray::__construct( $size )
```

**参数：**此函数接受指定数组大小的单个参数**$size**。

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的 SplFixedArray：：__Construct()函数：

**程序 1：**

```php
<?php

// Create new fixed array of size 2
$gfg = new SplFixedArray(2);

$gfg[1] = "GeeksforGeeks";

// Print Result 
var_dump($gfg[0]);
var_dump($gfg[1]);

?>
```

**输出：**

```php
NULL
string(13) "GeeksforGeeks"

```

**程序 2：**

```php
<?php

// Create new fixed array of size 8
$gfg = new SplFixedArray(8);

$gfg[2] = 5;
$gfg[4] = "gfg";
$gfg[5] = "Geeks";
$gfg[7] = "GeeksforGeeks";

// Iterate array and print its values
foreach( $gfg as $i ) {
    var_dump($i);
}
?>
```

**输出：**

```php
NULL
NULL
int(5)
NULL
string(3) "gfg"
string(5) "Geeks"
NULL
string(13) "GeeksforGeeks"

```

**引用：**[https://www.php.net/manual/en/splfixedarray.construct.php](https://www.php.net/manual/en/splfixedarray.construct.php)