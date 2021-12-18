# PHP|Ds\Map__Construct()函数

> Original: [https://www.geeksforgeeks.org/php-dsmap-__construct-function/](https://www.geeksforgeeks.org/php-dsmap-__construct-function/)

**ds\Map：：__Construction()**函数是 PHP 中的内置函数，用于创建新实例。

**语法：**

```php
public Ds\Map::__construct( $values )
```

**参数：**此函数接受单个参数**$values**，该参数保存要使用初始值的可遍历对象或数组。

以下程序说明了 PHP 中的**ds\Map：：__Construction()**函数：

**程序 1：**

```php
<?php 
// PHP program to illustrate the __construct() 
// function of Ds\map 

// Declare a new Map 
$map = new \Ds\Map(); 

// Display the map elements
print_r($map); 

// Creating a Map 
$map = new \Ds\Map([
    "1" => "Geeks",  
    "2" => "for",
    "3" => "Geeks"
]); 

// Display the map elements
print_r($map); 

?> 
```

**Output:**

```php
Ds\Map Object
(
)
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => 1
            [value] => Geeks
        )

    [1] => Ds\Pair Object
        (
            [key] => 2
            [value] => for
        )

    [2] => Ds\Pair Object
        (
            [key] => 3
            [value] => Geeks
        )

)

```

**程序 2：**

```php
<?php 
// PHP program to illustrate the __construct() 
// function of Ds\map 

// Creating a Map 
$map = new \Ds\Map(["1" => "10", 
            "2" => "20", "3" => 30]); 

// Display key-value pair 
print_r($map); 

// Creating another Map 
$map = new \Ds\Map([1 => "Welcome", 
            2 => "to", 3 => "GeeksforGeeks"]); 

// Display key-value pair 
print_r($map); 

?> 
```

**输出：**

```php
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => 1
            [value] => 10
        )

    [1] => Ds\Pair Object
        (
            [key] => 2
            [value] => 20
        )

    [2] => Ds\Pair Object
        (
            [key] => 3
            [value] => 30
        )

)
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => 1
            [value] => Welcome
        )

    [1] => Ds\Pair Object
        (
            [key] => 2
            [value] => to
        )

    [2] => Ds\Pair Object
        (
            [key] => 3
            [value] => GeeksforGeeks
        )

)

```

**引用：**[https://www.php.net/manual/en/ds-map.construct.php](https://www.php.net/manual/en/ds-map.construct.php)