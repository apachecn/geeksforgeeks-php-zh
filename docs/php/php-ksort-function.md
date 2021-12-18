# PHP|kort()函数

> Original: [https://www.geeksforgeeks.org/php-ksort-function/](https://www.geeksforgeeks.org/php-ksort-function/)

Kort()函数是 PHP 中的一个内置函数，用于根据数组的键值按**升序**对数组进行排序。 它以保持指数和值之间的关系的方式进行排序。

**语法：**

```
bool ksort( $array, $sorting_type )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$array:** this parameter specifies the array to be sorted. This is a required parameter.
*   **$SOLING_TYPE:** this is an optional parameter. There are different types of sorting discussed below:
    *   **SORT_Regular: the value of** *$SORT_TYPE* is SORT_Regular, and then compare items normally.
    *   **SORT_NUMERIC: the value of** *$SORT_TYPE* is SORT_NUMERIC, and then compare the items numerically.
    *   **SORT_STRING: the value of** *$SORT_TYPE* is SORT_STRING, and then compare items as strings.
    *   **SORT_LOCALE_STRING: the value of** *$SORT_TYPE* is SORT_STRING, and then compare items as strings based on the current locale.

**返回值：**此函数成功时返回 True，失败时返回 False。

下面的程序演示了 PHP 中的 kort()函数。

**程序 1：**

```
<?php
// PHP program to illustrate
// ksort()function

// Input different array elements
$arr = array("13" =>"ASP.Net",
             "12" =>"C#",
             "11" =>"Graphics",
             "4" =>"Video Editing",
             "5" =>"Photoshop",
             "6" =>"Article",
             "4" =>"Placement",
             "8" =>"C++",
             "7" =>"XML",
             "10" =>"Android",
             "1" =>"SQL",
             "2" =>"PL/Sql",
             "3" =>"End",
             "0" =>"Java",       
        );

// Implementation of ksort()
ksort($arr);

// for-Loop for displaying result
foreach ($arr as $key => $val) {
    echo "[$key] = $val";
    echo"\n";
}

?>
```

**输出：**

```
[0] = Java
[1] = SQL
[2] = PL/Sql
[3] = End
[4] = Placement
[5] = Photoshop
[6] = Article
[7] = XML
[8] = C++
[10] = Android
[11] = Graphics
[12] = C#
[13] = ASP.Net

```

**程序 2：**

```

<?php
// PHP program to illustrate
// ksort function

// Input different array elements
$arr = array("z" => 11,
             "y" => 22,
             "x" => 33,
             "n" => 44,
             "o" => 55,
             "b" => 66,
             "a" => 77,
             "m" => 2,
             "q" => -11,
             "i" => 3,
             "e" => 56,
             "d" => 1,                            
        );

// Implementation of ksort
ksort($arr);

// for-Loop for displaying result
foreach ($arr as $key => $val) {
    echo "[$key] = $val";
    echo"\n";
}

?>
```

**输出：**

```
[a] = 77
[b] = 66
[d] = 1
[e] = 56
[i] = 3
[m] = 2
[n] = 44
[o] = 55
[q] = -11
[x] = 33
[y] = 22
[z] = 11

```

**相关文章：**

*   [asort () function](https://www.geeksforgeeks.org/php-asort-function/)
*   [ukort () function](https://www.geeksforgeeks.org/php-uksort-function/)
*   [usort () function](https://www.geeksforgeeks.org/php-usort-function/)

**引用：**[http://php.net/manual/en/function.ksort.php](http://php.net/manual/en/function.ksort.php)