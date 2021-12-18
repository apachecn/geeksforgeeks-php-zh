# PHP|ds\Map diff()函数

> Original: [https://www.geeksforgeeks.org/php-dsmap-diff-function/](https://www.geeksforgeeks.org/php-dsmap-diff-function/)

**ds\Map：：diff()**函数是 PHP 中的一个内置函数，用于使用键创建一个映射，该键包含第一个映射中不存在于另一个映射中的元素。

**语法：**

```php
*Ds\Map* public Ds\Map::diff( $map )
```

**参数：**此函数接受单个参数**$map**，该参数用于保存需要排除其值的映射元素。

**返回值：**它返回一个新映射，其中包含第一个映射中不存在于另一个映射中的元素。

以下程序说明了 PHP 中的**ds\Map：：diff()**函数：

**程序 1：**

```php
<?php 
// PHP program to illustrate the diff() 
// function of Ds\map 

// Creating a Map 
$map1 = new \Ds\Map(["1" => "10", 
            "3" => 30, "4" => 40]); 

// Creating another Map 
$map2 = new \Ds\Map(["2" => "20",
        "3" => 35, "5" => 50, "6" => 60]); 

echo "Difference between two map: <br>";

print_r($map1 -> diff($map2));

?> 
```

**Output:**

```php
Difference between two map: 
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => 1
            [value] => 10
        )

    [1] => Ds\Pair Object
        (
            [key] => 4
            [value] => 40
        )

)

```

**程序 2：**

```php
<?php 
// PHP program to illustrate the diff() 
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

echo "Difference between two map: <br>";

print_r($map1 -> diff($map2));

?> 
```

**Output:**

```php
Difference between two map: 
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => 1
            [value] => Geeks
        )

)

```

**引用：**[https://www.php.net/manual/en/ds-map.diff.php](https://www.php.net/manual/en/ds-map.diff.php)