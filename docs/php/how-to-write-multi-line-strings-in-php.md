# 如何用 PHP 编写多行字符串？

> 原文:[https://www . geesforgeks . org/how-write-多行字符串-in-php/](https://www.geeksforgeeks.org/how-to-write-multi-line-strings-in-php/)

多行字符串可以通过以下方式用 PHP 编写。

1.  **使用转义序列:**我们可以使用\n 转义序列来声明字符串中的多行。

    **PHP 代码:**

    ## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

    ```php
    <?php
          //declaring multiple lines using the new line escape sequence
        $var="Geeks\nFor\nGeeks";
        echo $var;
    ?>
    ```

    **输出:**

    ```php
    Geeks
    For
    Geeks
    ```

2.  **使用串联赋值运算符:**我们可以使用串联赋值运算符 ***。=*** 连接两个字符串，用 PHP_EOL 标记行尾。

    **PHP 代码:**

    ## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

    ```php
    <?php
        $s1="Geeks". PHP_EOL;//PHP_EOL marks end of line so that
        $s2="For". PHP_EOL;//next string get concatenated as new line
        $s3="Geeks";
        $s1.=$s2.=$s3;//concatenating the string into $s1
        echo $s1;//printing final concatenated string
    ?>
    ```

    **输出:**

    ```php
    Geeks
    For
    Geeks
    ```

3.  **使用 Heredoc 和 Nowdoc 语法:**我们可以使用 PHP Heredoc 或 PHP Nowdoc 语法直接编写多行字符串变量。heredoc 和 nowdoc 的区别在于，heredoc 使用双引号字符串。对转义序列等的解析是在 heredoc 内部完成的，而 nowdoc 使用单引号字符串，因此不执行解析。

    **注意:**heredoc 和 nowdoc 语法中的分隔符必须始终位于一行的开头，不能有任何空格、字符等。

    **PHP 代码:**

    ## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

    ```php
    <?php
        // code
      //Heredoc variable
      $s1=<<<EOD
      Geeks
      \tFor
      Geeks
    EOD;
    echo $s1;
      echo"\n";
      //Nowdoc variable
      $s2=<<<'EOT'
      Geeks
      \tFor
      Geeks
    EOT;
    echo $s2
    ?>
    ```

    **输出:**

    ```php
     Geeks
          For
      Geeks
      Geeks
      \tFor
      Geeks
    ```

**参考文献:**[https://www . PHP . net/manual/en/language . types . string . PHP # language . types . string . syntax . now doc](https://www.php.net/manual/en/language.types.string.php#language.types.string.syntax.nowdoc)[https://www.geeksforgeeks.org/php-strings/](https://www.geeksforgeeks.org/php-strings/)