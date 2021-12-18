# PHP 数组 _search()函数

> 原文:[https://www.geeksforgeeks.org/php-array_search-function/](https://www.geeksforgeeks.org/php-array_search-function/)

在本文中，我们将看到如何使用 PHP 中的 *array_search()* 函数来搜索数组中的特定值&对应的返回键，&也将通过示例了解其实现。 **array_search()** 是 PHP 中的一个内置函数，用于搜索数组中的特定值，如果找到该值，它将返回其对应的键。如果有多个值，那么将返回第一个匹配值的键。

**语法** :

```php
array_search($value, $array, strict_parameter)
```

**参数:**该函数取如下三个参数:

*   **$ value:** This is a required field, the value to be searched in the index group.
*   **$ array:** This refers to the required field of the original array, which needs to be searched.
*   **Strict _ parameter (optional):** This is an optional field, which can be set to TRUE or FALSE, indicating the severity of the search. The default value of this parameter is false.
    *   If true, the function checks the same element, that is, the integer 10 will be treated differently from the string 10.
    *   If false, the strictness will not be maintained.

**返回值:**函数返回传递的对应值的键。如果没有找到，则返回 FALSE，如果有多个匹配项，则返回第一个匹配项。

**示例**:下面的程序说明了 PHP 中的 array_search()函数。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

  // PHP function to illustrate the use of array_search()
  function Search($value, $array)
  {
      return (array_search($value, $array));
  }
  $array = array(
      "ram",
      "aakash",
      "saran",
      "mohan",
      "saran"
  );
  $value = "saran";
  print_r(Search($value, $array));
?>
```

**输出** :

```php
2
```

**示例**:本示例说明了当 strict_parameter 设置为 FALSE 时函数的工作情况。请注意，数组和要搜索的元素的数据类型是不同的。

## PHP

```php
<?php

    // PHP function to illustrate the use of array_search()
    function Search($value, $array)
    {
        return (array_search($value, $array, false));
    }
    $array = array(
        45, 5, 1, 22, 22, 10, 10);
    $value = "10";
    print_r(Search($value, $array));
?>
```

**输出** :

```php
5
```

**示例**:在这个示例中，我们将利用上面的代码来找出如果我们将 strict _ 参数作为 TRUE 传递会发生什么。

## PHP

```php
<?php

    // PHP function to illustrate the use of array_search()
    function Search($value, $array)
    {
        return (array_search($value, $array, true));
    }
    $array = array(45, 5, 1, 22, 22, 10, 10);
    $value = "10";
    print_r(Search($value, $array));
?>
```

**输出** :

```php
No Output
```

**参考**:[http://php.net/manual/en/function.array-search.php](http://php.net/manual/en/function.array-search.php)