# PHP in_array()函数

> Original: [https://www.geeksforgeeks.org/php-in_array-function/](https://www.geeksforgeeks.org/php-in_array-function/)

在本文中，我们将了解如何在 PHP 中使用 in_array()函数查找数组中的值，并通过示例了解其实现。

**in_array()**函数是 PHP 中的内置函数，用于检查数组中是否存在给定值。 如果在给定数组中找到给定值，则返回 TRUE，否则返回 FALSE。

**语法**：

```
bool in_array( $val, $array_name, $mode )
```

**参数**：in_array()函数接受 3 个参数，其中 2 个是必需的，另外 1 个是可选的。 下面描述了所有三个参数：

*   **$val** : this is a required parameter that specifies the element or value to search for in a given array. This parameter can be a mixed type, that is, it can be a string type, an integer type, or any other type. If this parameter is a string type, the search is performed in a case-sensitive manner.
*   **$ARRAY_NAME** : this is a required parameter that specifies the array to search in.
*   **$mode** : optional parameter, Boolean. This parameter specifies the mode in which we want to perform the search. If set to true, the in_array () function searches for the same value type as the value specified by the $val parameter. The default value for this parameter is False.

**返回值**：in_array()函数返回一个布尔值，即如果在数组中找到值$val，则返回 TRUE，否则返回 FALSE。

**方法：**为了在数组中搜索特定值，我们将使用in_array()函数，其中用于搜索的参数是字符串类型&，其值设置为 true。 否则，如果在数组中未找到指定的值，则此函数返回FALSE 值。

通过这个例子，我们将理解 PHP 中 in_array()函数的概念。

**示例 1**：下面的程序在非严格模式下使用 in_array()函数执行搜索，即最后一个参数$mode 被设置为 False，这是它的默认值。 要搜索的值是字符串类型，而数组中的这个值是整数类型，因为搜索处于非严格模式，所以 in_array()函数仍返回 TRUE。

## PHP

```
<?php
  $marks = array(100, 65, 70, 87);
  if (in_array("100", $marks))
  {
    echo "found";
  }
  else
  {
    echo "not found";
  }
?>
```

**输出**

```
found
```

**示例 2**：下面的程序在严格模式下使用 in_array()函数执行搜索，即最后一个参数$mode 设置为 true，该函数现在还将检查值的类型。

## PHP

```
<?php
  $name = array("ravi", "ram", "rani", 87);

  if (in_array("ravi", $name, TRUE))
    {
    echo "found \n";
    }
  else
    {
    echo "not found \n";
    }

  if (in_array(87, $name, TRUE))
    {
    echo "found \n";
    }
  else
    {
    echo "not found \n";
    }

  if (in_array("87", $name, TRUE))
    {
    echo "found \n";
    }
  else
    {
    echo "not found \n";
    }
?>
```

**输出**

```
found 
found 
not found 
```

**参考**：[http://php.net/manual/en/function.in-array.php](http://php.net/manual/en/function.in-array.php)

PHP 是一种专门为 Web 开发设计的服务器端脚本语言。 您可以按照这个[PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和[PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。