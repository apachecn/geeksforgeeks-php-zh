# PHP | basename()函数

> 原文:[https://www.geeksforgeeks.org/php-basename-function/](https://www.geeksforgeeks.org/php-basename-function/)

PHP 中的 base name()函数是一个内置函数，如果文件的路径是作为 basename()函数的参数提供的，则该函数用于返回文件的基名称。

**语法:**

```
*string* basename ( $path , $suffix )
```

**参数:**PHP 中的 basename()函数接受两个参数，分别是路径和后缀。

1.  **$path** :此参数为字符串类型，为必选项。它指定文件的路径。
2.  **$后缀**:可选参数，以后缀结尾时隐藏文件扩展名。

**返回值:**该函数返回用户给定路径作为参数的文件的基本名称。

**错误和异常**:

1.  basename()函数无法识别路径组件，如“..”。
2.  basename()函数对用户提供的输入字符串进行操作，不知道实际的文件系统。
3.  在 windows 平台上，斜杠、正斜杠(/)和反斜杠(\)都用作目录分隔符，而在其他环境中，它只是正斜杠(/)。

**示例:**

```
Input : $path = "user01/home/documents/geeksforgeeks.php",
Output : geeksforgeeks.php

Input :  $path = "user01/home/documents/geeksforgeeks.php",
         $suffix = ".php"
Output : geeksforgeeks

```

下面的程序说明了 basename()函数:

**程序 1** :

```
<?php

$path = "user01/home/documents/geeksforgeeks.php";

// basename() function to show
// filename along with extension
echo basename($path);

?>
```

输出:

```
geeksforgeeks.php
```

**程序 2** :

```
<?php

$path = "user01/home/documents/geeksforgeeks.php";

// basename() function to show the
// filename while hiding the extension
echo basename($path, ".php");

?>
```

输出:

```
geeksforgeeks
```

**参考:**T2[http://php.net/manual/en/function.basename.php](http://php.net/manual/en/function.basename.php)