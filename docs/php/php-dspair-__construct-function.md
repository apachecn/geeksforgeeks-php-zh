# PHP|DS\Pair__Construct()函数

> Original: [https://www.geeksforgeeks.org/php-dspair-__construct-function/](https://www.geeksforgeeks.org/php-dspair-__construct-function/)

**Ds\Pair：：__Construct()函数**是 PHP 中的一个内置函数，用于创建一个新实例。

**语法：**

```php
*public* Ds\Pair::__construct( $key, $value )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$key:** this parameter holds the key of the Pair element.
*   **$value:** this parameter holds the value of the Pair element.

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的 Ds\Pair：：__Construct()函数：

**程序 1：**

```php
<?php 
// PHP program to illustrate the 
// Ds\Pair::__construct() function

// Declare a new pair 
$pair = new \Ds\Pair(); 

// Display the pair elements 
print_r($pair); 

// Creating another pair 
$pair = new \Ds\pair(
    ["1", "2", "3"],
    ["Geeks", "for", "Geeks"]
);

// Display the pair elements 
print_r($pair); 

?>
```

**输出：**

```php
Ds\Pair Object
(
    [key] => 
    [value] => 
)
Ds\Pair Object
(
    [key] => Array
        (
            [0] => 1
            [1] => 2
            [2] => 3
        )

    [value] => Array
        (
            [0] => Geeks
            [1] => for
            [2] => Geeks
        )

)

```

**程序 2：**

```php
<?php 
// PHP program to illustrate the 
// Ds\Pair::__construct() function

// Creating a pair 
$pair = new \Ds\pair(
    ["a", "b", "c"],
    ["10", "2", "30"]
);

// Display the pair elements 
var_dump($pair); 

?>
```

**输出：**

```php
object(Ds\Pair)#1 (2) {
  ["key"]=>
  array(3) {
    [0]=>
    string(1) "a"
    [1]=>
    string(1) "b"
    [2]=>
    string(1) "c"
  }
  ["value"]=>
  array(3) {
    [0]=>
    string(2) "10"
    [1]=>
    string(1) "2"
    [2]=>
    string(2) "30"
  }
}

```

**引用：**[https://www.php.net/manual/en/ds-pair.construct.php](https://www.php.net/manual/en/ds-pair.construct.php)