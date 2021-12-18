# PHP|ds\Map intersect()函数

> Original: [https://www.geeksforgeeks.org/php-dsmap-intersect-function/](https://www.geeksforgeeks.org/php-dsmap-intersect-function/)

**ds\Map：：Interect()**函数是 PHP 中的一个内置函数，用于创建包含与另一个地图的交集的新地图。

**语法：**

```php
*Ds\Map* public Ds\Map::intersect( Ds\Map $map )
```

**参数：**此函数接受单个参数**$map**，该参数保存包含其他元素键的另一个映射。

**返回值：**此函数返回当前地图与其他地图的交集。

下面的程序说明了 PHP 中的**ds\Map：：Intersect()**函数：

**程序 1：**

```php
<?php 
// PHP program to illustrate the intersect()
// function of Ds\map 

// Creating a Map 
$map1 = new \Ds\Map(["1" => "10", 
            "3" => 30, "4" => 40]); 

// Creating another Map 
$map2 = new \Ds\Map(["2" => "20",
        "3" => 35, "5" => 50, "6" => 60]); 

// Use Ds\Map::intersect() function
print_r($map1 -> intersect($map2));

?> 
```

**输出：**

```php
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => 3
            [value] => 30
        )

)

```

**程序 2：**

```php
<?php 
// PHP program to illustrate the intersect() 
// function of Ds\map 

// Creating a Map 
$map1 = new \Ds\Map([
    "1" => "Geeks",  
    "2" => "for",
    "3" => "Geeks"]);

// Creating another Map 
$map2 = new \Ds\Map([
    "2" => "for",
    "3" => "Geeks",
    "4" => "GeeksforGeeks"]);

// Use Ds\Map::intersect() function
print_r($map1 -> intersect($map2));

?> 
```

**输出：**

```php
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => 2
            [value] => for
        )

    [1] => Ds\Pair Object
        (
            [key] => 3
            [value] => Geeks
        )

)

```

**引用：**[https://www.php.net/manual/en/ds-map.intersect.php](https://www.php.net/manual/en/ds-map.intersect.php)