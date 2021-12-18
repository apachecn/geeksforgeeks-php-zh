# PHP|Join()函数

> Original: [https://www.geeksforgeeks.org/php-join-function/](https://www.geeksforgeeks.org/php-join-function/)

Join()函数是 PHP 中的内置函数，用于联接由字符串分隔的元素数组。

**语法**

```
*string* join( $separator, $array)
```

**参数**：Join()函数接受两个参数，其中一个是可选的，另一个是必需的。

*   **$分隔符：**这是一个可选参数，属于字符串类型。 数组的值将连接成一个字符串，并将由这里提供的*$Separator*参数分隔。 这是可选的，如果未提供，则默认为“”(即空字符串)
*   **$array：**要联接其值以形成字符串的数组。

**返回类型**：Join()函数的返回类型为 String。 它将返回由*$ARRAY*的元素组成的连接字符串。

例如：

```
Input : join(array('Geeks','for','Geeks')
Output : GeeksforGeeks

Input : join("-",array('Geeks','for','Geeks')
Output : Geeks-for-Geeks

```

下面的程序演示了 PHP 中 Join()函数的工作原理：

```
<?php
    // PHP Code to implement join function

    $InputArray = array('Geeks','for','Geeks');

    // Join without separator
    print_r(join($InputArray));

    print_r("\n");

    // Join with separator
    print_r(join("-",$InputArray));
?>
```

产出：

```
GeeksforGeeks
Geeks-for-Geeks

```