# 在 PHP 中 array_key()和 array_key_exists()有什么区别？

> 原文:[https://www . geeksforgeeks . org/array _ keys 和 array_key_exists-in-php/](https://www.geeksforgeeks.org/what-are-the-differences-between-array_keys-and-array_key_exists-in-php/) 有何区别

下面的文章指出了 PHP 中两个内置函数 [**array_keys()**](https://www.geeksforgeeks.org/php-array_keys-function/) 和[**array _ key _ exists()**](https://www.geeksforgeeks.org/php-array_key_exists-function/)的区别。

[**array_keys()函数:**](https://www.geeksforgeeks.org/php-array_keys-function/)**array _ keys(**)函数用于返回所有键或数组键的子集。该函数适用于索引数组和关联数组。

**语法:**

```php
array_keys(array, value, strict)
```

**参数:**

*   **数组:**一个带检查键的数组。
*   **值:**检索键的值。
*   **严格:**检查变量数据类型的参数。

**例 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
$arr = array(
    "Java" => "SpringBoot",
    "PHP 4.0" => "CodeIgniter",
    "Python" => "Django",
    "PHP 3.0" => "CodeIgniter"
);

// Searching for keys of codeigniter
$key1 = array_keys($arr, "CodeIgniter");
print("Keys for CodeIgniter : ");
print_r($key1);
print("</br>");

// Searching for keys of wordpress
$key2 = array_keys($arr, "WordPress");
print("Keys for WordPress : ");
print_r($key2);
?>
```

**输出:**

```php
Keys for CodeIgniter : Array ( [0] => PHP 4.0 [1] => PHP 3.0 )
Keys for WordPress : Array ( )
```

**例 2:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
  $arr = array(1, 2, 3, 4, 5);

  // Searching for keys of string 5
  // using strict parameter true
  $key1 = array_keys($arr, "5", true);
  print("Keys for '5' : ");
  print_r($key1);
  echo("</br>");

  // Searching for keys of string 5
  // using strict parameter false
  $key2 = array_keys($arr, "5", false);
  print("Keys for '5' : ");
  print_r($key2);
?>
```

**输出:**

```php
Keys for '5' : Array ( )
Keys for '5' : Array ( [0] => 4 )
```

[**array _ key _ exists()**](https://www.geeksforgeeks.org/php-array_key_exists-function/)**:**PHP 中的 **array_key_exists()** 方法用于验证指定键的数组。如果该键存在，则返回布尔值 *true* ，如果该键在数组中不存在，则返回 *false* 。

**语法:**

```php
array_key_exists(key, array)
```

**参数:**

*   **键:**要检查的数值。
*   **数组:**一个带检查键的数组。

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
  $arr = array(1, 2, 3, 4, 5);

  // Searching for keys of string 5
  $key1 = array_key_exists('4', $arr);
  if($key1) {
      echo("Key exists");
  }else {
      echo("Key does not exist");
  }
?>
```

**输出:**

```php
key exists
```

**差异:**上述两种方法之间存在以下差异:

<figure class="table">

| **数组 _ 键** | **array _ key _ exists** |
| --- | --- |
| It checks whether the corresponding value is mapped to any key in the array. | Check whether there is a key in the array. |
| It returns an array. | Returns a Boolean value. |
| It is suitable for one-dimensional and multi-dimensional arrays. | Only valid for one-dimensional arrays. |
| Strict parameters can be used. | Matching data types, unique values can be used. |
| Match, if the value parameter is empty, it can also be used to retrieve all the keys of the array. | It just checks the key specified in the array. |

</figure>