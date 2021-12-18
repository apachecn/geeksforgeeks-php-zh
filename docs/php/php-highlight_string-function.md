# PHP|Highlight_string()函数

> Original: [https://www.geeksforgeeks.org/php-highlight_string-function/](https://www.geeksforgeeks.org/php-highlight_string-function/)

Highlight_string()函数是 PHP 中的一个内置函数，用于突出显示文本字符串。 它返回 HTML 文本格式的输出。

**语法：**

```
highlight_string( $string, $return )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$string:** it is a required parameter to specify the text to highlight.
*   **$return:** optional parameters. If True, it provides highlighted code as a string rather than printing it on the screen.

**返回值：**如果为 True，则它将突出显示的代码作为字符串返回，否则在失败时返回 False。

下面的程序演示了 PHP 中的 Highlight_string()函数。

**程序 1：**

```
<?php
highlight_string('Welcome to Geeksforgeeks');
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php
highlight_string('<?php
// PHP Program to add two numbers

function Add( $x, $y)
{
    $sum = $x + $y; 

    return $sum;
}

    // Driver Code
    echo Add(15, 32);
?>')
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/function.highlight-string.php](http://php.net/manual/en/function.highlight-string.php)