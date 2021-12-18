# PHP|ds\Pair copy()函数

> Original: [https://www.geeksforgeeks.org/php-dspair-copy-function/](https://www.geeksforgeeks.org/php-dspair-copy-function/)

**ds\Pair：：copy()函数**是 PHP 中的一个内置函数，用于返回 Pair 元素的副本。

**语法：**

```
*Ds\Pair* Ds\Pair::copy( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回 Pair 元素的浅副本。

下面的程序说明了 PHP 中的 Ds\Pair：：Copy()函数：

**程序 1：**

```
<?php 

// Create new Pair
$pair = new \Ds\Pair("G", "GeeksforGeeks"); 

// Display the pair element 
print_r($pair); 

// Use copy() function 
$pair->copy(); 

echo "Copied pair elements:\n";

// Display the pair element 
print_r($pair); 

?> 
```

**输出：**

```
Ds\Pair Object
(
    [key] => G
    [value] => GeeksforGeeks
)
Copied pair elements:
Ds\Pair Object
(
    [key] => G
    [value] => GeeksforGeeks
)

```

**程序 2：**

```
<?php 

// Create new Pair
$pair = new \Ds\Pair(["G", "GeeksforGeeks"], [1, 2]); 

// Display the pair element 
var_dump($pair); 

// Use copy() function 
$pair->copy(); 

echo "Copied pair elements:\n";

// Display the pair element 
var_dump($pair); 

?> 
```

**输出：**

```
object(Ds\Pair)#1 (2) {
  ["key"]=>
  array(2) {
    [0]=>
    string(1) "G"
    [1]=>
    string(13) "GeeksforGeeks"
  }
  ["value"]=>
  array(2) {
    [0]=>
    int(1)
    [1]=>
    int(2)
  }
}
Copied pair elements:
object(Ds\Pair)#1 (2) {
  ["key"]=>
  array(2) {
    [0]=>
    string(1) "G"
    [1]=>
    string(13) "GeeksforGeeks"
  }
  ["value"]=>
  array(2) {
    [0]=>
    int(1)
    [1]=>
    int(2)
  }
}

```

**引用：**[https://www.php.net/manual/en/ds-pair.copy.php](https://www.php.net/manual/en/ds-pair.copy.php)