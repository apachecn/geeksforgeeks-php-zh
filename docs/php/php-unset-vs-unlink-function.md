# PHP|unset()与 Unlink()函数

> Original: [https://www.geeksforgeeks.org/php-unset-vs-unlink-function/](https://www.geeksforgeeks.org/php-unset-vs-unlink-function/)

这两个函数都用于执行一些撤消操作，但在不同的情况下使用会导致两个操作都不同。 当您想要完全删除文件时，可以使用[unlink()函数](https://www.geeksforgeeks.org/php-unlink-function/)。 当您想要使文件为空时，可以使用[unset()函数](https://www.geeksforgeeks.org/php-unset-function/)。
**Unlink()函数：**Unlink()函数是 PHP 中内置的函数，用于删除文件。 必须删除的文件的文件名作为参数发送，函数成功时返回 True，失败时返回 False。 PHP 中的 unlink()函数接受两个参数。
**语法：**和

```
unlink( filename, context )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **filename：**这是一个必选参数，用于指定必须删除的文件的文件名。
*   **上下文：**这是一个可选参数，指定可用于修改流性质的文件句柄的上下文。

**返回值：**成功返回 True，失败返回 False。
假设有一个名为**‘gfg.txt’**
**的文件示例：**和

## PHP

```
<?php

// PHP program to delete a file named gfg.txt
// using unlink() function

$file_pointer = fopen('gfg.txt');

// Writing on a file named gfg.txt
fwrite($file_pointer, 'A computer science portal for geeks!');
fclose($file_pointer);

// Using unlink() function to delete a file
unlink('gfg.txt');

?>
```

发帖主题：Re：Колибри0.7.8.0

```
1
```

**注意：**如果我们没有访问文件“gfg.txt”的权限，则 unlink()函数会在失败时生成 E_WARNING 级别的错误。
**unset()函数：**unset()函数是 PHP 中的一个内置函数，用于通过清空文件来删除文件中的内容。 这意味着该功能会清除文件的内容，而不是删除它。 函数的作用是：不仅清除文件内容，还用于取消变量的设置，从而使其为空。
**语法：**和

```
unset( $variable )
```

**参数：**此函数接受所需的单个参数**变量**。 它是需要取消设置的变量。
**返回值：**此函数不返回任何值。
**示例：**和

## PHP

```
<?php

$var = "hello";

// Change would be reflected outside the function 
function unset_value() {
    unset($GLOBALS['var']);
}

unset_value();
echo $var;
?>
```

发帖主题：Re：Колибри0.7.8.0

```
No output
```

**unlink()和 unset()函数的区别：**、
、

<figure class="table">

| Unlink () function | Unset () function |
| It is used to completely delete the files in the directory when the execution is successful. | Used to make a specific file empty by deleting its contents. |
| There are two parameters, **fileName** , and the other parameter is **Context** . | There is only one parameter **variable** . |
| True is returned for success and False for failure. | This function does not return any value. |
| This is a file system handler. | This is a variable management function. |

</figure>