# PHP|krort()函数

> Original: [https://www.geeksforgeeks.org/php-krsort-function/](https://www.geeksforgeeks.org/php-krsort-function/)

Krort()函数是 PHP 中的一个内置函数，用于根据数组的索引值按键按**逆序**对数组进行排序。 它以保持指数和值之间的**关系的方式进行排序。**

**语法：**

```
bool krsort( $array, $sorting_type )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$array：**此参数指定要排序的数组。 这是必选参数。
*   **$SOLING_TYPE：**这是一个可选参数。 下面将讨论不同的分类类型：
    *   **SORT_Regular：***$SORT_TYPE*的值为 SORT_Regular，则正常比较项目。
    *   **SORT_NUMERIC：***$SORT_TYPE*的值是 SORT_NUMERIC，然后对项目进行数值比较。
    *   **SORT_STRING：***$SORT_TYPE*的值是 SORT_STRING，则将项目作为字符串进行比较。
    *   **SORT_LOCALE_STRING：***$SORT_TYPE*的值是 SORT_STRING，然后根据当前区域设置将项目作为字符串进行比较。

**返回值：**此函数成功时返回 True，失败时返回 False。

下面的程序演示了 PHP 中的 krort()函数。
**程序 1：**

```
<?php
// PHP program to illustrate
// krsort()function

// Input different array elements
$arr = array("0" =>"Technology",
             "1" =>"Machine",
             "2" =>"GeeksforGeeks",
             "3" =>"Graphics",
             "4" =>"Videos",
             "5" =>"Report",
             "6" =>"Article",
             "7" =>"Placement",
             "8" =>"Contribute",
             "9" =>"Reset",
             "10" =>"Copy",
        );

// Implementation of krsort()
krsort($arr);

// for-Loop for displaying result
foreach ($arr as $key => $val) {
    echo "[$key] = $val";
    echo"\n";
}

?>
```

**Output:**

```
[10] = Copy
[9] = Reset
[8] = Contribute
[7] = Placement
[6] = Article
[5] = Report
[4] = Videos
[3] = Graphics
[2] = GeeksforGeeks
[1] = Machine
[0] = Technology

```

**程序 2：**

```
<?php
// PHP program to illustrate
// krsort function

// Input different array elements
$arr = array("a" => 11,
             "b" => 22,
             "d" => 33,
             "n" => 44,
             "o" => 55,
             "p" => 66,
             "r" => 77,
             "s" => 2,
             "q" => -11,
             "t" => 3,
             "u" => 1000,
             "z" => 1,                            
        );
// Implementation of krsort
krsort($arr);

// for-Loop for displaying result
foreach ($arr as $key => $val) {
    echo "[$key] = $val";
    echo"\n";
}

?>
```

**Output:**

```
[z] = 1
[u] = 1000
[t] = 3
[s] = 2
[r] = 77
[q] = -11
[p] = 66
[o] = 55
[n] = 44
[d] = 33
[b] = 22
[a] = 11

```

**相关文章：**

*   [排序()函数](https://www.geeksforgeeks.org/php-sort-function/)
*   [asort()函数](https://www.geeksforgeeks.org/php-asort-function/)
*   [arort()函数](https://www.geeksforgeeks.org/php-arsort-function/)

**引用：**[http://php.net/manual/en/function.krsort.php](http://php.net/manual/en/function.krsort.php)