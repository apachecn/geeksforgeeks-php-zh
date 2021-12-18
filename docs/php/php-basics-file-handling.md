# PHP |文件处理基础知识

> 原文:[https://www.geeksforgeeks.org/php-basics-file-handling/](https://www.geeksforgeeks.org/php-basics-file-handling/)

任何应用程序都需要文件处理。有些任务需要处理文件。PHP 中的文件处理类似于使用任何编程语言(如 c 语言)进行文件处理。PHP 有许多功能可以处理普通文件。这些职能是:

1)**fopen()–**PHP fopen()函数用于打开一个文件。fopen()的第一个参数包含要打开的文件的名称，第二个参数说明需要打开文件的模式，例如，

```
<?php
$file = fopen(“demo.txt”,'w');
?>
```

文件可以在以下任何模式下打开:

*   **“w”–**打开一个仅用于写入的文件。如果文件不存在，则创建新文件，如果文件已经存在，则清除文件内容。
*   **“r”–**文件以只读方式打开。
*   **“a”–**文件只为写入而打开。文件指针指向文件结尾。文件中的现有数据将被保留。
*   **“w+”–**打开文件进行读写。如果文件不存在，则创建新文件，如果文件已经存在，则清除文件内容。
*   **“r+”–**文件打开读/写。
*   **“a+”–**文件打开进行写入/读取。文件指针指向文件结尾。文件中的现有数据将被保留。如果文件不在那里，则创建新文件。
*   **“x”–**创建的新文件仅用于写入。

2)**fread()–**–使用 fopen()打开文件后，使用 fread()读取数据内容。它需要两个参数。一个是文件指针，另一个是以字节为单位的文件大小，

```
<?php
$filename = "demo.txt";
$file = fopen( $filename, 'r' );
$size = filesize( $filename );
$filedata = fread( $file, $size );
?>
```

3)**fwrite()–**可以使用 fwrite()函数创建新文件或向现有文件添加文本。fwrite()函数的参数是文件指针和要写入文件的文本。它可以包含可选的第三个参数，其中指定了要写入的文本长度，例如，

```
<?php
$file = fopen("demo.txt", 'w');
$text = "Hello world\n";
fwrite($file, $text);
?>
```

4)**fclose()–**文件使用 fclose()功能关闭。它的参数是需要关闭的文件，例如，

```
<?php
$file = fopen("demo.txt", 'r');
//some code to be executed
fclose($file);
?>
```

**参考–**
[维基百科](https://en.wikibooks.org/wiki/PHP_and_MySQL_Programming/File_Handling)

本文由 **Swasthik** 供稿。如果你喜欢极客博客并想投稿，你也可以用 contribute.geeksforgeeks.org 写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。