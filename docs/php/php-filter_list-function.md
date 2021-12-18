# PHP|filter_list()函数

> Original: [https://www.geeksforgeeks.org/php-filter_list-function/](https://www.geeksforgeeks.org/php-filter_list-function/)

Filter_list()函数是 PHP 中的一个内置函数，用于返回所有支持的筛选器的列表。

**语法：**

```
*array* filter_list( void )
```

**参数：**此函数不接受任何参数。

**返回值：**它返回一个包含支持的筛选器的所有名称的数组。 如果它返回空数组，则不包含任何筛选器。 过滤器 id 可以通过 filter_id()函数获得。

**注意：**此函数适用于 PHP 5.2.0 及更新版本。

以下示例说明了 PHP 中的 filter_id()函数：

**示例 1：**

```
<?php
print_r(filter_list());
?>
```

**Output:**

```
Array
(
    [0] => int
    [1] => boolean
    [2] => float
    [3] => validate_regexp
    [4] => validate_domain
    [5] => validate_url
    [6] => validate_email
    [7] => validate_ip
    [8] => validate_mac
    [9] => string
    [10] => stripped
    [11] => encoded
    [12] => special_chars
    [13] => full_special_chars
    [14] => unsafe_raw
    [15] => email
    [16] => url
    [17] => number_int
    [18] => number_float
    [19] => magic_quotes
    [20] => callback
)

```

**示例 2：**它在单个列表中显示所有筛选器的关联 ID。

```
<?php

// Array filter function assign to a variable
$arr = filter_list();

// Use loop to display the key and its value
while (list ($key, $val) = each ($ar2)) {
echo "$key -> $val : ( ".filter_id($val). " ) <br>";
}

?>
```

**Output:**

```
0 -> int : ( 257 ) 
1 -> boolean : ( 258 ) 
2 -> float : ( 259 ) 
3 -> validate_regexp : ( 272 ) 
4 -> validate_domain : ( 277 ) 
5 -> validate_url : ( 273 ) 
6 -> validate_email : ( 274 ) 
7 -> validate_ip : ( 275 ) 
8 -> validate_mac : ( 276 ) 
9 -> string : ( 513 ) 
10 -> stripped : ( 513 ) 
11 -> encoded : ( 514 ) 
12 -> special_chars : ( 515 ) 
13 -> full_special_chars : ( 522 ) 
14 -> unsafe_raw : ( 516 ) 
15 -> email : ( 517 ) 
16 -> url : ( 518 ) 
17 -> number_int : ( 519 ) 
18 -> number_float : ( 520 ) 
19 -> magic_quotes : ( 521 ) 
20 -> callback : ( 1024 ) 

```

**引用：**[http://php.net/manual/en/function.filter-list.php](http://php.net/manual/en/function.filter-list.php)