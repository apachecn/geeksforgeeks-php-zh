# PHP | array _ ui intersect()函数

> 原文:[https://www . geeksforgeeks . org/PHP-array _ uiintersect-function/](https://www.geeksforgeeks.org/php-array_uintersect-function/)

**array _ uiintersection()**是 PHP 中的一个内置函数，用于根据值计算两个或多个数组的交集。在用户定义函数的帮助下，将第一个数组值与所有其他数组进行比较，并返回匹配项。

**语法:**

```php
array_uintersect($array1, $array2, $array3, ..... $arrayn, user_function
```

**参数:**该函数接受两种类型的参数。一个是数组列表，另一个是用户定义的函数。

*   **数组列表**:这个函数接受一个数组列表，数组之间用空格隔开，我们要找到数组的交集。在上面的语法中，数组的列表是 *$array1，$array2，$array3，…..$arrayn* 。它可以接受任意数量的由空格分隔的数组，最小数量为 2。
*   **user_function:** 这是一个字符串类型参数，是用户定义函数的名称。当参数中的值相同时，函数返回 0，如果第一个参数大于第二个参数，则返回 1，否则返回-1。

**返回值:**该函数返回另一个数组，该数组包含第一个数组中作为参数传递的所有其他数组中存在的所有元素。如果没有元素匹配，则返回空数组。

示例:

```php
Input : $a1=array("a"=>"striver", "b"=>"geeks", "d"=>"raj")
        $a2=array("d"=>"articles", "e"=>"raj", "f"=>"coding")

Output :
Array
(
    [d] => raj
)

Input :$a1 = array("1"=>"geeks", "2"=>"for", "3"=>"geek", "4"=>"coding")
$a2 = array("1"=>"geeks", "2"=>"for", "3"=>"php", "4"=>"coding", "5"=>"ide")
$a3 = array("6"=>"cpp", "7"=>"java", 8=>"geeks")

Output :
Array
(
    [1] => geeks
)

```

下面的程序说明了 array _ uiintersection()函数:

**程序 1:** 演示 array _ uiintersection()函数工作原理的 PHP 程序。

```php
<?php
// PHP program to demonstrate the working of 
// array_uintersect() function  

// user-defined function
function user_function($a, $b)
{
if ($a===$b)
  {
  return 0;
  }
  return ($a>$b)?1:-1;
}

// arrays 
$a1=array("a"=>"striver", "b"=>"geeks", "d"=>"raj");
$a2=array("d"=>"articles", "e"=>"raj", "f"=>"coding");

$result=array_uintersect($a1, $a2, "user_function");
print_r($result);
?>
```

**输出:**

```php
Array
(
    [d] => raj
)
```

**程序二:**用三个数组演示 array _ uiintersection()函数工作的 PHP 程序。

```php
<?php
// PHP program to demonstrate the working of 
// array_uintersect() function with 3 arrays 

// user-defined function
function user_function($a, $b)
{
if ($a===$b)
  {
  return 0;
  }
  return ($a>$b)?1:-1;
}

// 3 arrays 
$a1 = array("1"=>"geeks", "2"=>"for", "3"=>"geek",
                                    "4"=>"coding");
$a2 = array("1"=>"geeks", "2"=>"for", "3"=>"php",
                        "4"=>"coding", "5"=>"ide");
$a3 = array("6"=>"cpp", "7"=>"java", 8=>"geeks");

$result=array_uintersect($a1, $a2, $a3, "user_function");
print_r($result);
?>
```

**输出:**

```php
Array
(
    [1] => geeks
)
```

**参考**:
T3】http://php.net/manual/en/function.array-uintersect.php