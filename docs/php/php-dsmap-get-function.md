# PHP|ds\Map get()函数

> Original: [https://www.geeksforgeeks.org/php-dsmap-get-function/](https://www.geeksforgeeks.org/php-dsmap-get-function/)

**ds\Map：：Get()**函数是 PHP 中的一个内置函数，用于返回给定键的值。

**语法：**

```php
*mixed* public Ds\Map::get( mixed $key[, mixed $default] )
```

**参数：**此函数接受两个参数，如上所述，如下所述：

*   **$key:** it holds the key of the value to be returned.
*   **$DEFAULT:** optional parameter, returned if KEY is not found.

**返回值：**此函数返回与给定键映射的值，如果找不到键，则返回默认值。

以下程序说明了 PHP 中的**ds\Map：：Get()**函数：

**程序 1：**

```php
<?php 
// PHP program to illustrate the get()
// function of Ds\map 

// Creating a Map 
$map = new \Ds\Map([
        1 => 10, 
        2 => 20,
        3 => 30, 
        4 => 40,
        5 => 50]); 

// Use Ds\Map::get() function
var_dump($map->get(1));
var_dump($map->get(3));
var_dump($map->get(5));
var_dump($map->get(7, 100));

?> 
```

**输出：**

```php
int(10)
int(30)
int(50)
int(100)

```

**程序 2：**

```php
<?php 

// Creating a Map 
$map = new \Ds\Map([
    "a" => "Geeks",  
    "b" => "for",
    "c" => "Geeks"
]); 

// Use Ds\Map::get() function
var_dump($map->get("a"));
var_dump($map->get("b"));
var_dump($map->get("c"));
var_dump($map->get("d", "GeeksforGeeks"));

?> 
```

**输出：**

```php
string(5) "Geeks"
string(3) "for"
string(5) "Geeks"
string(13) "GeeksforGeeks"

```

**引用：**[https://www.php.net/manual/en/ds-map.get.php](https://www.php.net/manual/en/ds-map.get.php)