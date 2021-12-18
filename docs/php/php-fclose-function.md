# PHP|flose()函数

> Original: [https://www.geeksforgeeks.org/php-fclose-function/](https://www.geeksforgeeks.org/php-fclose-function/)

PHP 中的 flose()函数是一个内置函数，用于关闭由打开的文件指针指向的文件。 函数的作用是：成功时返回 TRUE，失败时返回 FALSE。 它将该文件作为必须关闭的参数，然后关闭该文件。

**语法：**

```php
*bool* fclose( $file )
```

**参数：**PHP 中的 flose()函数只接受一个参数，即$file。 此参数指定必须关闭的文件。

**返回值：**成功返回 TRUE，失败返回 FALSE。

**错误和异常**：

1.  如果文件是通过 fwrite()函数写入的，则必须首先使用 flose()函数关闭该文件，并且您必须读取该文件的内容。
2.  The fclose() function in PHP doesn’t works for remote files.It only works on files which are accessible by the server’s filesystem.

    **示例：**

    ```php
    Input : $check = fopen("gfg.txt", "r");
            fclose($check);
    Output : true

    Input: $check = fopen("singleline.txt", "r");
           $seq = fgets($check);
           while(! feof($check))
           {
             echo $seq ;
             $seq = fgets($check);
           }
           fclose($check);
    Output:true

    ```

    以下程序说明了 flose()函数：

    **程序 1**：

    ```php
    <?php

    // opening a file using fopen() function
    $check = fopen("gfg.txt", "r");

    // closing a file using fclose() function
    fclose($check);

    ?>
    ```

    产出：

    ```php
    true
    ```

    **程序 2**：在下面的程序中，名为*singleline.txt*的文件只包含一行“该文件只包含一行”。

    ```php
    <?php

    // a file is opened using fopen() function
    $check = fopen("singleline.txt", "r");
    $seq = fgets($check);

    // Outputs a line of the file until
    // the end-of-file is reached
    while(! feof($check))
    {
      echo $seq ;
      $seq = fgets($check);
    }

    // the file is closed using fclose() function
    fclose($check);

    ?>
    ```

    产出：

    ```php
    This file consists of only a single line.

    ```

    **参考**：
    [http://php.net/manual/en/function.fclose.php](http://php.net/manual/en/function.fclose.php)