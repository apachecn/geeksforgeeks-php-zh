# PHP | asort()函数

> 原文:[https://www.geeksforgeeks.org/php-asort-function/](https://www.geeksforgeeks.org/php-asort-function/)

asort()函数是 PHP 中的一个内置函数，用于根据值对数组进行排序。它的排序方式是保持指数和值之间的关系。默认情况下，它按照值的**升序**排序。

**语法:**

```
bool asort( $array, $sorting_type )
```

**参数:**该函数接受两个参数，如上所述，如下所述:

*   **$array:** 此参数指定要排序的数组。这是一个强制参数。
*   **$sorting_type:** 这是可选参数。下面讨论了不同的排序类型:
    *   **排序 _ 常规:***$排序 _ 类型*的值为排序 _ 常规，则项目比较正常。
    *   **排序 _ 数值:***$排序 _ 类型*的值为排序 _ 数值，然后对项目进行数值比较。
    *   **排序 _ 字符串:***$排序 _ 类型*的值为排序 _ 字符串，则项目作为字符串进行比较。
    *   **排序 _ 区域设置 _ 字符串:***$排序 _ 类型*的值是排序 _ 字符串，然后根据当前区域设置将项目作为字符串进行比较。

**返回值:**该函数成功返回真，失败返回假。

下面的程序说明了 PHP 中的 asort()函数。
**节目一:**

```
<?php
// PHP program to illustrate
// asort() function

// Input different array elements
$arr = array("0" => "Web Technology",
            "1" => "Machine Learing",
            "2" => "GeeksforGeeks",
            "3" => "Computer Graphics",
            "4" => "Videos",
            "5" => "Report Bug",
            "6" => "Article",
            "7" => "Sudo Placement",
            "8" => "SContribute",
            "9" => "Reset",
            "10" => "Copy",
            "11" => "IDE",
            "12" => "Gate Note",
        );

// Implementation of asort()
asort($arr);

// for-Loop for displaying result
foreach ($arr as $key => $val) {
    echo "[$key] = $val";
    echo"\n";
}

?>
```

**Output:**

```
[6] = Article
[3] = Computer Graphics
[10] = Copy
[12] = Gate Note
[2] = GeeksforGeeks
[11] = IDE
[1] = Machine Learing
[5] = Report Bug
[9] = Reset
[8] = SContribute
[7] = Sudo Placement
[4] = Videos
[0] = Web Technology

```

**程序 2:**

```
<?php
// PHP program to illustrate
// asort() function

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
// Implementation of asort()
asort($arr);

// for-Loop for displaying result
foreach ($arr as $key => $val) {
    echo "[$key] = $val";
    echo"\n";
}

?>
```

**Output:**

```
[q] = -11
[z] = 1
[s] = 2
[t] = 3
[a] = 11
[b] = 22
[d] = 33
[n] = 44
[o] = 55
[p] = 66
[r] = 77
[u] = 1000

```

**相关文章:**

*   [排序()功能](https://www.geeksforgeeks.org/php-sort-function/)
*   [arsort()功能](https://www.geeksforgeeks.org/php-arsort-function/)
*   [uksort()功能](https://www.geeksforgeeks.org/php-uksort-function/)
*   [usort()功能](https://www.geeksforgeeks.org/php-usort-function/)

**参考:**T2】http://php.net/manual/en/function.asort.php