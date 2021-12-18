# PHP 中的 count()和 sizeof()函数有什么不同？

> 原文:[https://www . geeksforgeeks . org/PHP 中函数的计数和大小有什么不同/](https://www.geeksforgeeks.org/what-is-the-different-between-count-and-sizeof-functions-in-php/)

PHP 中的集合对象由一个长度参数来表征，以指示其中包含的元素数量。为了执行数组操作和修改，需要估计数组的长度。

[**sizeof()方法**](https://www.geeksforgeeks.org/php-sizeof-function/)**:**sizeof()方法用于计算数组或任何其他可数对象中存在的所有元素。它既可用于一维阵列，也可用于多维阵列。

```php
sizeof(arr, mode)
```

**参数:**该方法接受下面讨论的两个参数:

*   **arr–**对元素进行计数的数组。
*   **模式–**指示器，检查是否计数所有元素–
    *   0–默认。不计算多维数组的所有元素
    *   1–递归计数数组(计数多维数组的所有元素)

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
$arr = array(
       "Java" => array(
           "SpringBoot",
           "Eclipse"
       ),
       "Python"=>array(
           "Django"   
       ),
       "PHP"=>array(
           "CodeIgniter"
       )
); 

print_r($arr);
print("<br>");

echo "Sub elements of an array: " 
      . sizeof($arr) . "<br>";
echo "All elements of an array: "
      . sizeof($arr, 1);

?>
```

**输出:**

```php
Array ( 
    [Java] => Array ( 
        [0] => SpringBoot 
        [1] => Eclipse 
    ) 
    [Python] => Array ( 
        [0] => Django 
    ) 
    [PHP] => Array ( 
        [0] => CodeIgniter 
    ) 
)
Sub elements of an array: 3
All elements of an array: 7
```

[**count()方法**](https://www.geeksforgeeks.org/php-count-function/)**:**count()方法用于计算数组或任何其他可数对象中的所有元素。它既可用于一维阵列，也可用于多维阵列。

```php
count(arr, mode)
```

**参数:**该方法接受下面讨论的两个参数:

*   **arr–**对元素进行计数的数组。
*   **模式–**指示器，检查是否计数所有元素–
    *   0–默认。不计算多维数组的所有元素
    *   1–递归计数数组(计数多维数组的所有元素)

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
$arr = array(
       "Java" => array(
      "SpringBoot",
      "Eclipse"
       ),
       "Python" => array(
           "Django"   
       ),
       "PHP" => array(
           "CodeIgniter"
       )
); 

print_r($arr);
print("<br>");

echo "Sub elements of an array: " 
      . count($arr) . "<br>";
echo "All elements of an array: "
      . count($arr, 1);

?>
```

**输出**

```php
Array ( 
    [Java] => Array ( 
        [0] => SpringBoot 
        [1] => Eclipse 
    ) 
    [Python] => Array ( 
        [0] => Django 
    ) 
    [PHP] => Array ( 
        [0] => CodeIgniter 
    ) 
)
Sub elements of an array: 3
All elements of an array: 7
```

**sizeof()和 count()方法的区别:**

*   sizeof()方法需要较长的执行时间。
*   sizeof()方法是 count()方法的别名。