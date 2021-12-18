# 在 PHP

中删除空数组元素的程序

> Original: [https://www.geeksforgeeks.org/program-to-remove-empty-array-elements-in-php/](https://www.geeksforgeeks.org/program-to-remove-empty-array-elements-in-php/)

给定一个包含元素的数组。 任务是从数组中删除空元素，如空字符串或 NULL 元素。

**方法 1：**使用[array_filter()函数](https://www.geeksforgeeks.org/php-array_filter-function/)。 它是通过使用 arrayfilter()函数实现的。 当使用回调函数声明时，它还会删除 FALSE 值，但是，如果未指定回调函数，则将删除数组中等于 FALSE 的所有值，例如空字符串或 NULL 值。

**示例：**

```php
<?php

// Declare array and stored array value
$array = array("geeks", 11, '', null, 12, 
            "for", 1997, false, "geeks");

// Function to remove empty elements
// from array
$filtered_array = array_filter($array);

// Display the filtered array
var_dump($filtered_array);
?>
```

**Output:**

```php
array(6) {
  [0]=>
  string(5) "geeks"
  [1]=>
  int(11)
  [4]=>
  int(12)
  [5]=>
  string(3) "for"
  [6]=>
  int(1997)
  [8]=>
  string(5) "geeks"
}

```

**方法 2：**使用[unset()函数](https://www.geeksforgeeks.org/php-unset-function/)。 另一种方法是使用 EMPTY()函数和 unset()函数从数组中删除空元素。 函数的作用是：检查元素是否为空。

**示例：**

```php
<?php

// Declare array and stored array value
$array = array("geeks", 11, '', null, 12, 
           "for", 1997, false, "geeks");

// Loop to find empty elements and 
// unset the empty elements
foreach($array as $key => $value)         
    if(empty($value))
        unset($array[$key]);

// Display the array elements        
foreach($array as $key => $value)         
    echo ($array[$key] . "<br>");
?>
```

**Output:**

```php
geeks
11
12
for
1997
geeks

```