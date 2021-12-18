# PHP|sha1_file()函数

> Original: [https://www.geeksforgeeks.org/php-sha1_file-function/](https://www.geeksforgeeks.org/php-sha1_file-function/)

Sha1_file()函数是 PHP 中的一个内置函数，用于生成文本文件的 SHA-1 散列。 此函数在成功时返回字符串，否则返回 False。

**语法：**

```
sha1_file ( $file, $raw )
```

**使用的参数：**此函数接受两个参数，如上所述，如下所述。

*   **$FILE：**它是指定 SHA1 哈希的文件的强制参数。
*   **$RAW：**它是一个可选参数，用于指定布尔值。
    *   **true-**原始 20 个字符的二进制格式。
    *   **FALSE-默认情况下为**。 40 个字符的十六进制数字。

**返回值：**函数成功时返回 SHA1 散列字符串，否则返回 FALSE。

假设有一个名为*“gfg.txt”*的文件，其内容如下。

> 发布您自己的
> 文章，并与
> 世界分享
> 知识！！

下面的程序演示了 sha1_file()函数。

**程序 1：**

```
<?php
// PHP  program to illustrate 
// sha1_file() function

$gfg = sha1_file("gfg.txt");

echo $gfg;

?>
```

发帖主题：Re：Колибри0.7.8.0

```
989aa47ec7ea68605dca25b499c8414e283e8354

```

**程序 2：**，可选参数$RAW，值 TRUE 和 FALSE 不同。

```
<?php
// PHP  program to illustrate 
// sha1_file() function

// Without optional parameter
echo sha1_file("gfg.txt") . "\n";

// with optional parameter $raw = FALSE (by default)
// no changes in result
echo sha1_file("gfg.txt", FALSE) . "\n";

// with optional parameter $raw = TRUE 
// result changed
echo sha1_file("gfg.txt", TRUE) . "\n";

?>
```

发帖主题：Re：Колибри0.7.8.0

```
989aa47ec7ea68605dca25b499c8414e283e8354
989aa47ec7ea68605dca25b499c8414e283e8354
???~??h`]?%???AN(>?T

```

**引用：**[http://php.net/manual/en/function.sha1-file.php](http://php.net/manual/en/function.sha1-file.php)