# PHP|fgets()函数

> Original: [https://www.geeksforgeeks.org/php-fgets-function/](https://www.geeksforgeeks.org/php-fgets-function/)

PHP 中的 fgets()函数是一个内置函数，用于从打开的文件返回一行。

*   它用于从文件指针返回一行，并在指定长度、文件末尾(EOF)或新行(以先到者为准)停止返回。
*   要读取的文件和要读取的字节数作为参数发送给 fgets()函数，它从用户指定的文件返回一个长度为-1 字节的字符串。
*   It returns False on failure.

    **语法：**

    ```php
    fgets(file, length)

    Parameters Used:
    The fgets() function in PHP accepts two parameters.
    file : It specifies the file from which characters have 
    to be extracted. 
    length : It specifies the number of bytes to be 
    read by the fgets() function. The default value 
    is 1024 bytes.
    ```

    **返回值：**它从用户指向的文件返回一个长度为-1 字节的字符串，如果失败则返回 False。

    **错误和异常**

    1.  该函数没有针对大文件进行优化，因为它一次读取一行，并且可能需要很长时间才能完全读取长文件。
    2.  如果多次使用 fgets()函数，则必须清除缓冲区。
    3.  Fgets()函数返回布尔值 False，但很多时候它返回的是非布尔值，计算结果为 False。

    假设有一个名为“gfg.txt”的文件，它包含：

    > 这是第一行。
    > 这是第二行。
    > 这是第三行。

    **程序 1**

    ```php
    <?php
    // file is opened using fopen() function
    $my_file = fopen("gfg.txt", "rw");

    // Prints a single line from the opened file pointer
    echo fgets($my_file);

    // file is closed using fclose() function
    fclose($my_file);
    ?>
    ```

    发帖主题：Re：Колибри0.7.0

    ```php
    This is the first line.
    ```

    **程序 2**

    ```php
    <?php
    //file is opened using fopen() function
    $my_file = fopen("gfg.txt", "rw");

    // prints a single line at a time until end of file is reached
    while (! feof ($my_file))
      {
      echo fgets($my_file);
      }

    // file is closed using fclose() function
    fclose($my_file);
    ?>
    ```

    发帖主题：Re：Колибри0.7.0

    ```php
    This is the first line.
    This is the second line.
    This is the third line.

    ```

    **引用：**
    [http://php.net/manual/en/function.fgets.php](http://php.net/manual/en/function.fgets.php)