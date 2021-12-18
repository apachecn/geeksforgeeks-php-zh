# PHP|file_put_content()函数

> Original: [https://www.geeksforgeeks.org/php-file_put_contents-function/](https://www.geeksforgeeks.org/php-file_put_contents-function/)

PHP 中的 FILE_PUT_CONTENTS()函数是一个内置函数，用于将字符串写入文件。 函数的作用是：检查用户想要写入的文件，如果该文件不存在，则创建一个新文件。

用户想要写入的文件的路径和必须写入的数据作为参数发送给函数，成功时返回写入文件的字节数，失败时返回 FALSE。

**语法：**

```
file_put_contents($file, $data, $mode, $context)
```

**参数：**PHP 中的 file_put_content()函数接受两个强制参数和两个可选参数。

1.  **$file**：它指定要写入的文件。
2.  **$data**：它指定必须写入文件的数据。 它可以是字符串、数组或数据流。
3.  **$CONTEXT**：它是一个可选参数，用于指定自定义上下文或流的行为。
4.  **$mode**：这是一个可选参数，用于指定数据必须如何写入文件，如 FILE_USE_INCLUDE_PATH、FILE_APPEND、LOCK_EX。

**返回值：**它返回成功时写入文件的字节数，失败时返回 False。

**错误和异常**：

1.  函数的作用是：返回布尔值 FALSE，但也可能返回计算结果为 FALSE 的非布尔值。
2.  如果提供的目录无效，则此函数无法写入内容。

例如：

```
Input : file_put_contents("gfg.txt", "A computer 
                     science portal for geeks!");
Output : 36

Input : $file_pointer = 'gfg.txt';
        $open = file_get_contents($file_pointer);
        $open .= "A computer science portal for geeks!";
        file_put_contents($file_pointer, $open);
Output : 36

```

下面的程序演示了 file_put_content()函数。

**程序 1**：

```
<?php

// writing content on gfg.txt
echo file_put_contents("gfg.txt", "A computer 
                  science portal for geeks!");
?>
```

产出：

```
36
```

**程序 2**：

```
<?php

$file_pointer = 'gfg.txt';

// Open the file to get existing content
$open = file_get_contents($file_pointer);

// Append a new person to the file
$open .= "A computer science portal for geeks!";

// Write the contents back to the file
file_put_contents($file_pointer, $open);

?>
```

产出：

```
36
```

**引用：**
[http://php.net/manual/en/function.file-put-contents.php](http://php.net/manual/en/function.file-put-contents.php)