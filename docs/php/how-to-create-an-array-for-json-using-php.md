# 如何用 PHP 为 JSON 创建数组？

> 原文:[https://www . geeksforgeeks . org/如何使用-php/](https://www.geeksforgeeks.org/how-to-create-an-array-for-json-using-php/) 为 json 创建数组

在本文中，我们将看到如何在 PHP 中为 JSON 创建一个数组，并将通过示例看到它的实现。

[**Array:**](https://www.geeksforgeeks.org/php-arrays/)PHP 中的 Array 是一种数据结构，它允许我们在单个变量下存储多个数据类型相似的元素，从而节省了我们为每个数据创建不同变量的工作量。数组有助于创建相似类型的元素列表，可以使用它们的索引或键来访问这些元素。使用 PHP 中的 [**数组()**函数](https://www.geeksforgeeks.org/php-array-function/)创建一个数组。PHP 中有 3 种数组类型，如下所示:

*   索引数组:它是一个带有数字键的数组。它基本上是一个数组，其中每个键都与它自己的特定值相关联。
*   [关联数组](https://www.geeksforgeeks.org/associative-arrays-in-php/):用于存储键值对。
*   [多维数组](https://www.geeksforgeeks.org/multidimensional-arrays-in-php/):是一种在每个索引处存储另一个数组而不是单个元素的数组类型。换句话说，将多维数组定义为数组的数组。

为此，我们将使用关联数组，该数组使用键值类型结构来存储数据。这些键将是一个字符串或整数，用作在数组中搜索相应值的索引。 [json_encode()](https://www.geeksforgeeks.org/php-json_encode-function/) 函数用于将数组的值转换为 json。这个函数是从 PHP5 中添加进来的。此外，您可以根据自己的需求进行更多的数组嵌套。也可以用这个函数创建一个对象数组的数组。就像在 JSON 中一样，所有的东西都存储为一个键值对，我们将把这些 PHP 数组的键值对转换为 JSON，它可以用来发送来自 REST API 服务器的响应。

**示例 1:** 下面的示例是将一个数组转换为 JSON。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

  // Create an array that contains another
  // array with key value pair
  $arr = array (

      // Every array will be converted
      // to an object
      array(
          "name" => "Pankaj Singh",
          "age" => "20"
      ),
      array(
          "name" => "Arun Yadav",
          "age" => "21"
      ),
      array(
          "name" => "Apeksha Jaiswal",
          "age" => "20"
      )
  );

  // Function to convert array into JSON
  echo json_encode($arr);
?>
```

**Output:** 

```php
[{"name":"Pankaj Singh","age":"20"},
{"name":"Arun Yadav","age":"21"},
{"name":"Apeksha Jaiswal","age":"20"}]
```

**示例 2:** 此示例说明了将 2D 关联数组转换为 JSON。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

  // Declare two dimensional associative
  // array and initialize it
  $arr = array (
      "first"=>array(
          "id"=>1,
          "product_name"=>"Doorbell",
          "cost"=>199
      ),
      "second"=>array(
          "id"=>2,
          "product_name"=>"Bottle",
          "cost"=>99
      ),
      "third"=>array(
          "id"=>3,
          "product_name"=>"Washing Machine",
          "cost"=>7999
      )
  );

  // Function to convert array into JSON
  echo json_encode($arr);
?>
```

**Output:** 

```php
{"first":{"id":1,"product_name":"Doorbell","cost":199},
"second":{"id":2,"product_name":"Bottle","cost":99},
"third":{"id":3,"product_name":"Washing Machine","cost":7999}}
```