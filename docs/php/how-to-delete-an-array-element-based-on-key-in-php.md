# PHP 中如何删除基于键的数组元素？

> 原文:[https://www . geesforgeks . org/如何删除基于 php 中键元素的数组/](https://www.geeksforgeeks.org/how-to-delete-an-array-element-based-on-key-in-php/)

给定一个数组(一维或多维)，任务是根据键值删除数组元素。

**示例:**

```
Input: Array
       (   
           [0] => 'G' 
           [1] => 'E'
           [2] => 'E'
           [3] => 'K'
           [4] => 'S'
       )
       Key = 2
Output: Array
        (   
            [0] => 'G' 
            [1] => 'E'
            [3] => 'K'
            [4] => 'S'
        )

```

**使用 [unset()函数](https://www.geeksforgeeks.org/php-unset-function/):**unset()函数用于从数组中移除元素。unset 函数用于销毁任何其他变量，并以同样的方式删除数组中的任何元素。这个 unset 命令将数组键作为输入，并从数组中移除该元素。移除后，关联的键和值不会改变。

**语法:**

```
unset($variable)
```

**参数:**本功能接受单参数*变量*。它是必需的参数，用于取消设置元素。

**程序 1:** 从一维数组中删除一个元素。

```
<?php
// PHP program to delete an array 
// element based on index

// Declare arr variable
// and initialize it
$arr = array('G', 'E', 'E', 'K', 'S');

// Display the array element
print_r($arr);

// Use unset() function delete
// elements
unset($arr[2]);

// Display the array element
print_r($arr);

?>
```

**Output:**

```
Array
(
    [0] => G
    [1] => E
    [2] => E
    [3] => K
    [4] => S
)
Array
(
    [0] => G
    [1] => E
    [3] => K
    [4] => S
)

```

**程序 2:** 从关联数组中删除一个元素。

```
<?php 

// PHP program to creating two 
// dimensional associative array 
$marks = array( 

    // Ankit will act as key 
    "Ankit" => array( 

        // Subject and marks are 
        // the key value pair 
        "C" => 95, 
        "DCO" => 85, 
    ), 

    // Ram will act as key 
    "Ram" => array( 

        // Subject and marks are 
        // the key value pair 
        "C" => 78, 
        "DCO" => 98, 
    ), 

    // Anoop will act as key 
    "Anoop" => array( 

        // Subject and marks are 
        // the key value pair 
        "C" => 88, 
        "DCO" => 46, 
    ), 
); 

echo "Before delete the element <br>";

// Display Results
print_r($marks); 

// Use unset() function to
// delete elements
unset($marks["Ram"]);

echo "After delete the element <br>";

// Display Results
print_r($marks); 

?> 
```

**Output:**

```
Before delete the element 
Array
(
    [Ankit] => Array
        (
            [C] => 95
            [DCO] => 85
        )

    [Ram] => Array
        (
            [C] => 78
            [DCO] => 98
        )

    [Anoop] => Array
        (
            [C] => 88
            [DCO] => 46
        )

)
After delete the element 
Array
(
    [Ankit] => Array
        (
            [C] => 95
            [DCO] => 85
        )

    [Anoop] => Array
        (
            [C] => 88
            [DCO] => 46
        )

)

```

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。