# PHP|stripslash()函数

> Original: [https://www.geeksforgeeks.org/php-stripslashes-function/](https://www.geeksforgeeks.org/php-stripslashes-function/)

Stripslash()函数是 PHP 中的内置函数。 此函数用于删除字符串中的反斜杠。
**语法：**

```
stripslashes(string)
```

**参数：**此函数只接受一个参数，如上面的语法所示。 具体说明如下：

*   **字符串：**这是指定函数将在其上操作的字符串的唯一必需参数。

**返回值：**此函数返回去掉反斜杠的字符串。

例如：

```
Input : "Geeks for\ Geeks"
Output : Geeks for Geeks

Input : "A\ Computer \Science \Portal"
Output : A Computer Science Portal

```

下面的程序演示了 PHP 中的 stripslash()函数：

**程序 1：**

```
<?php
    //code
    $str = "Geeks for\ Geeks";
    echo stripslashes($str);
?>
```

产出：

```
Geeks for Geeks
```

**程序 2：**在此程序中，我们将看到 stripslash()函数的数组实现。 Stripslash()不是递归的。 为了将此函数应用于数组，需要使用递归函数。

```
<?php
function stripslashes_arr($value)
{
    $value = is_array($value) ?
                array_map('stripslashes_arr', $value) :
                stripslashes($value);

    return $value;
}

$array = array("Gee\\ks ", "fo\\r", " \\Geeks");
$array = stripslashes_arr($array);

print_r($array);
?>
```

产出：

```
Array
(
    [0] => Geeks 
    [1] => for
    [2] =>  Geeks
)

```

**引用：**
[http://php.net/manual/en/function.stripslashes.php](http://php.net/manual/en/function.stripslashes.php)