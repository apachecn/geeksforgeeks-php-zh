# PHP|Implode()函数

> Original: [https://www.geeksforgeeks.org/php-implode-function/](https://www.geeksforgeeks.org/php-implode-function/)

Implode()是 PHP 中的一个内置函数，用于联接数组的元素。 Implode()是[PHP|Join()函数](https://www.geeksforgeeks.org/php-join-function/)的别名，其工作方式与 Join()函数完全相同。

如果我们有一个元素数组，我们可以使用 implode()函数将它们连接起来形成一个字符串。 我们基本上是用字符串连接数组元素。 与 Join()函数一样，implode()函数也返回由数组元素组成的字符串。

**语法**：

```
*string* implode(separator,array)

```

**参数**：implode()函数接受两个参数，其中一个是可选的，另一个是必需的。

1.  **Delimiter** : optional parameter, string type. The values of the array are concatenated into a string and separated by the *delimiter* parameter provided here. This is optional and defaults to "" (that is, an empty string) if it is not provided.
2.  **array** : an array whose values are to be joined to form a string.

**注**：implode()的分隔符参数是可选的。 但是，为了向后兼容，建议始终使用两个参数。

**返回类型**：implode()函数的返回类型为 String。 它将返回由*数组*的元素组成的连接字符串。

示例：

```
Input : implode(array('Geeks','for','Geeks')
Output : GeeksforGeeks

Input : implode("-",array('Geeks','for','Geeks')
Output : Geeks-for-Geeks

```

下面的程序演示了 PHP 中的 implode()函数的工作原理：

```
<?php
    // PHP Code to implement join function

    $InputArray = array('Geeks','for','Geeks');

    // Join without separator
    print_r(implode($InputArray));

    print_r("\n");

    // Join with separator
    print_r(implode("-",$InputArray));
?>
```

帖子主题：Re：Колибри

**参考**：[http://php.net/manual/en/function.implode.php](http://php.net/manual/en/function.implode.php)