# PHP | array_count_values()函数

> 原文:[https://www . geesforgeks . org/PHP-array _ count _ values-function/](https://www.geeksforgeeks.org/php-array_count_values-function/)

array_count_values()是 PHP 中的一个内置函数，用于对数组中的所有值进行计数。换句话说，我们可以说 array_count_values()函数用于计算数组中所有元素的频率。

**语法:**

```php
*array* array_count_values( $array )

```

**参数:**该功能接受单参数**$数组**。这个参数是我们需要计算其中存在的值的计数的数组。

**返回值:**这个函数返回一个带有键值对的关联数组，其中键是作为参数传递的数组元素，值是这些元素在数组中的出现频率。

**注意:**如果元素不是字符串或整数，则抛出 E_WARNING。

**例:**

```php
Input : array = ("Geeks", "for", "Geeks", "Geeks", "Welcome", "for")
Output : 
        Array
        (
          [Geeks] => 3
          [for] => 2
          [Welcome] => 1
        )

Input : array = (1, 1, 2, 3 , 1 , 2 , 4, 5)
Output :
       Array
       (
         [1] => 3
         [2] => 2
         [3] => 1
         [4] => 1
         [5] => 1
       ) 

```

下面的程序说明了 PHP 中 array_count_values()函数的工作方式:

```php
<?php

// PHP code to illustrate the working
// of array_count_values() function
function Counting($array){
    return(array_count_values($array));
}

// Driver Code
$array = array("Geeks", "for", "Geeks", "Geeks", "Welcome", "for");
print_r(Counting($array));

?>
```

**输出:**

```php
Array
(
    [Geeks] => 3
    [for] => 2
    [Welcome] => 1
)

```

**参考:**T2】http://php.net/manual/en/function.array-count-values.php