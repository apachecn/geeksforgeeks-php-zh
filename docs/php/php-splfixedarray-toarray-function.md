# PHP|SplFixedArray toArray()函数

> Original: [https://www.geeksforgeeks.org/php-splfixedarray-toarray-function/](https://www.geeksforgeeks.org/php-splfixedarray-toarray-function/)

**SplFixedArray：：toArray()**函数是 PHP 中的一个内置函数，用于从固定数组中获取 PHP 数组。

**语法：**

```
*array* SplFixedArray::toArray()
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回 PHP 数组。

以下程序说明了 PHP 中的**SplFixedArray：：toArray()**函数：

**程序 1：**

```
<?php

// Create a fixed size array
$gfg = new SplFixedArray(3);

$gfg[0] = 1;
$gfg[1] = 5;
$gfg[2] = 10;

var_dump($gfg->toArray());
?>
```

**输出：**

```
array(3) {
  [0]=>
  int(1)
  [1]=>
  int(5)
  [2]=>
  int(10)
}

```

**程序 2：**

```
<?php

// Create some fixed size array
$gfg = new SplFixedArray(3);

$gfg1 = new SplFixedArray(6);
$gfg1[0] = 1;
$gfg1[1] = 5;
$gfg1[2] = 10;

$gfg2 = new SplFixedArray(5);
$gfg2[0] = 1;
$gfg2[1] = 5;
$gfg2[2] = 10;
$gfg2[3] = 10;
$gfg2[4] = 20;

// Print result
var_dump($gfg->toArray());
var_dump($gfg1->toArray());
var_dump($gfg2->toArray());

?>
```

**输出：**

```
array(3) {
  [0]=>
  NULL
  [1]=>
  NULL
  [2]=>
  NULL
}
array(6) {
  [0]=>
  int(1)
  [1]=>
  int(5)
  [2]=>
  int(10)
  [3]=>
  NULL
  [4]=>
  NULL
  [5]=>
  NULL
}
array(5) {
  [0]=>
  int(1)
  [1]=>
  int(5)
  [2]=>
  int(10)
  [3]=>
  int(10)
  [4]=>
  int(20)
}

```

**引用：**[https://www.php.net/manual/en/splfixedarray.toarray.php](https://www.php.net/manual/en/splfixedarray.toarray.php)