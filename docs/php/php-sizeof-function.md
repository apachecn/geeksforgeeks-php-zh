# PHP sizeof()函数

> Original: [https://www.geeksforgeeks.org/php-sizeof-function/](https://www.geeksforgeeks.org/php-sizeof-function/)

在本文中，我们将了解如何使用 PHP 中的**sizeof()**函数获取数组长度。 **sizeof()**函数是 PHP 中的一个内置函数，用于计算数组或任何其他可数对象中存在的元素数。

**语法：**

```
int sizeof(array, mode);
```

**参数：**此函数接受 2 个参数，如下所述：

*   **array** : this parameter represents an array of elements to be counted.
*   **mode** : this is an optional parameter that specifies the mode of the function. You can take two different values, as follows:
    *   **0** : default value, all elements of the multidimensional array are not counted
    *   **1** : recursive count array (calculates all elements of a multidimensional array)

**返回值：**此函数返回语法中所示的整数值，表示数组中存在的元素数。

通过示例，我们将理解**sizeof()**函数的概念。

**示例 1**：此示例说明了一维数组中元素数的计数。

## PHP

```
<?php
   // input array
   $a=array(1,2,3,4,5,6);

   // getting total number of elements
   // present in the array.
   $result = sizeof($a);

   print($result);
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例**：此示例说明了如何计算多维数组中的元素数。

## PHP

```
<?php
  $array = array('name' => array('Geeks', 'For', 'Geeks'),
                'article' => array('sizeof', 'function', 'PHP'));

  // Recursive count
  echo sizeof($array, 1);

  // Normal count
  echo sizeof($array);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/function.sizeof.php](http://php.net/manual/en/function.sizeof.php)