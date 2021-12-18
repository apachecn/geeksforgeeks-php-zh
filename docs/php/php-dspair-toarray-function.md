# PHP|ds\Pair toArray()函数

> Original: [https://www.geeksforgeeks.org/php-dspair-toarray-function/](https://www.geeksforgeeks.org/php-dspair-toarray-function/)

**ds\Pair：：toArray()函数**是 PHP 中的一个内置函数，用于将 Pair 元素转换为关联数组。 此函数不会修改实际的配对。 此方法返回一个数组，该数组的值不会更改元素的顺序。

**语法：**

```php
*array* Ds\Pair::toArray( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回通过转换 Pair 元素生成的关联数组。

下面的程序说明了 PHP 中的 Ds\Pair：：toArray()函数：

**程序 1：**

```php
<?php 

// Declare a Pair 
$pair = new \Ds\Pair("a", "GeeksforGeeks"); 

// Corresponding array is 
echo "Array is:\n"; 
print_r($pair->toArray()); 

?> 
```

**输出：**

```php
Array is:
Array
(
    [key] => a
    [value] => GeeksforGeeks
)

```

**程序 2：**

```php
<?php 

// Declare a Pair 
$pair = new \Ds\Pair([1, 2], ["GeeksforGeeks", "Welcome"]); 

// Corresponding array is 
echo "Array is:\n"; 
var_dump($pair->toArray()); 

?> 
```

**输出：**

```php
Array is:
array(2) {
  ["key"]=>
  array(2) {
    [0]=>
    int(1)
    [1]=>
    int(2)
  }
  ["value"]=>
  array(2) {
    [0]=>
    string(13) "GeeksforGeeks"
    [1]=>
    string(7) "Welcome"
  }
}

```

**引用：**[https://www.php.net/manual/en/ds-pair.toarray.php](https://www.php.net/manual/en/ds-pair.toarray.php)