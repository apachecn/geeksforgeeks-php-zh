# PHP | copy()函数

> 原文:[https://www.geeksforgeeks.org/php-copy-function/](https://www.geeksforgeeks.org/php-copy-function/)

PHP 中的 copy()函数是一个内置函数，用于复制指定的文件。它将源文件复制到目标文件，如果目标文件已经存在，它将被覆盖。copy()函数在成功时返回 true，在失败时返回 false。

**语法:**

```
bool copy ( $source, $dest )
```

**参数:**PHP 中的 copy()函数接受两个参数，分别是源和目的。

1.  **$source** :指定源文件的路径。
2.  **$dest** :用于指定目标文件的路径。

**返回值:**成功返回真，失败返回假。

**错误和异常**:

1.  PHP 中的 copy()函数不适用于远程文件。它只对服务器文件系统可访问的文件起作用。
2.  如果目标文件已经存在，它将被覆盖。

**示例:**

```
Input : echo copy("gfg.txt", "geeksforgeeks.txt");
Output : true

Input : $srcfile = '/user01/Desktop/admin/gfg.txt';
        $destfile = 'user01/Desktop/admin/geeksforgeeks.txt';
        echo copy($srcfile, $destfilefile);
Output : true

```

以下程序说明了 copy()功能:

**程序 1** :

```
<?php

// Copying gfg.txt to geeksforgeeks.txt
echo copy("gfg.txt", "geeksforgeeks.txt");

?>
```

输出:

```
true
```

**程序 2** :

```
<?php

// Copying gfg.txt to geeksforgeeks.txt
$srcfile = '/user01/Desktop/admin/gfg.txt';
$destfile = 'user01/Desktop/admin/geeksforgeeks.txt';

if (!copy($srcfile, $destfilefile)) {
    echo "File cannot be copied! \n";
}
else {
    echo "File has been copied!";
}

?>
```

输出:

```
File has been copied!
```

**参考:**T2[http://php.net/manual/en/function.copy.php](http://php.net/manual/en/function.copy.php)