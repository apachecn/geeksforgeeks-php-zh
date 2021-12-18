# PHP|ds\Map Capacity()函数

> Original: [https://www.geeksforgeeks.org/php-dsmap-capacity-function/](https://www.geeksforgeeks.org/php-dsmap-capacity-function/)

**ds\Map：：Capacity(**)函数是 PHP 中的内置函数，用于返回地图的当前容量。

**语法：**

```php
*int* public Ds\Map::capacity( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回 MAP 当前的容量。

下面的程序演示了 PHP 中的**ds\Map：：Capacity()**函数：

**程序：**

```php
<?php 

// Declare a map 
$map = new \Ds\Map(); 

// Use capacity() function 
var_dump($map->capacity()); 

// Creating a Map 
$map = new \Ds\Map(["1" => "Geeks",  
            "2" => "for", "3" => "Geeks"]); 

// Use capacity() function 
var_dump($map->capacity());

?> 
```

**输出：**

```php
int(8)
int(8)

```

**引用：**[https://www.php.net/manual/en/ds-map.capacity.php](https://www.php.net/manual/en/ds-map.capacity.php)