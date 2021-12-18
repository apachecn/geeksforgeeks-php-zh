# PHP|Dechex()函数

> Original: [https://www.geeksforgeeks.org/php-dechex-function/](https://www.geeksforgeeks.org/php-dechex-function/)

Dechex()是 PHP 中的一个内置函数，用于将给定的十进制数转换为等效的十六进制数。 函数名称中的单词“dechex”代表十进制到十六进制。 函数的作用是：只处理无符号数字。 如果传递给它的参数是负数，则它会将其视为无符号数。
可以转换的最大数字是十进制的 4294967295，结果是“FFFFFFF”。

**语法：**

```
*string* dechex($value)
```

**参数：**此函数接受单个参数*$value*。 它是要转换为十六进制表示的十进制数字。

**返回值：**它返回作为参数传递给它的数字的十六进制字符串表示。

例如：

```
Input : dechex(10)
Output : a

Input : dechex(47)
Output : 2f

Input : dechex(4294967295)
Output : ffffffff

```

下面的程序演示了 PHP 中的 dechex()函数：

*   Passing 10 as a parameter:

    ```
    <?php

    echo dechex(10);

    ?>    
    ```

    产出：

    ```
    a
    ```

*   Passing 47 as a parameter:

    ```
    <?php

    echo dechex(47);

    ?>      
    ```

    产出：

    ```
    2f
    ```

*   When the largest possible decimal number is passed as a parameter:

    ```
    <?php

    echo dechex(4294967295);

    ?>      
    ```

    产出：

    ```
    ffffffff
    ```

**参考**：
[http://php.net/manual/en/function.dechex.php](http://php.net/manual/en/function.dechex.php)