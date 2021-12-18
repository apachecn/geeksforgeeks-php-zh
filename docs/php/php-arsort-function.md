# PHP | arsort()函数

> 原文:[https://www.geeksforgeeks.org/php-arsort-function/](https://www.geeksforgeeks.org/php-arsort-function/)

PHP 中的 arsort()用于根据值对数组进行排序。它的排序方式是保持指数和值之间的关系。默认情况下，它按照值的**降序**排序。

**语法:**

```
bool arsort( $array, $sorting_type )
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **$ array:** This parameter specifies the array to sort. This is a mandatory parameter.
*   **$ sorting _ type:** This parameter specifies the name of the user-defined function that will be used to sort the keys of array $array. This comparison function must return an integer.

**返回值:**该函数成功返回真，失败返回假。

下面的程序说明了 PHP 中的 arsort()函数。

**程序 1:**

```
<?php
// PHP program to illustrate
// arsort() function

// Input different array elements
$arr = array("0" => "GeeksforGeeks",
             "1" => "Practice",
             "2" => "Contribute",
             "3" => "Java",
             "4" => "Videos",
             "5" => "Report Bug",
             "6" => "Article",
             "7" => "Sudo Placement"
        );

// Implementation of arsort()
arsort($arr);

// for-Loop  for displaying result
foreach ($arr as $key => $val) {
    echo "[$key] = $val";
    echo"\n";
}

?>
```

**输出:**

```
[4] = Videos
[7] = Sudo Placement
[5] = Report Bug
[1] = Practice
[3] = Java
[0] = GeeksforGeeks
[2] = Contribute
[6] = Article

```

**程序二:**

```
<?php
// PHP program to illustrate
// arsort() function

// Input different array elements
$arr = array("a" => 11,
             "b" => 22,
             "d" => 33,
             "n" => 44,
             "o" => 55,
             "p" => 66,
             "p" => 77,
             "q" => 88,
        );
// Implementation of arsort()
arsort($arr);

// for-Loop  for displaying result
foreach ($arr as $key => $val) {
    echo "[$key] = $val";
    echo"\n";
}

?>
```

**输出:**

```
[q] = 88
[p] = 77
[o] = 55
[n] = 44
[d] = 33
[b] = 22
[a] = 11

```

**相关文章:**

*   [uksort（）函数](https://www.geeksforgeeks.org/php-uksort-function/)
*   [乌阿 sort()范雎](https://www.geeksforgeeks.org/php-uasort-function/)
*   [使用地点()](https://www.geeksforgeeks.org/php-usort-function/)

**参考:**T2】http://php.net/manual/en/function.arsort.php