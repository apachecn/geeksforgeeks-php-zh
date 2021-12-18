# PHP | bindec()函数

> 原文:[https://www.geeksforgeeks.org/php-bindec-function/](https://www.geeksforgeeks.org/php-bindec-function/)

在处理数字时，很多时候我们需要转换数字的基数，其中最常用的转换是二进制到十进制的转换。为此，PHP 为我们提供了一个内置函数 bindec()。PHP 中的 *bindec()* 函数用来返回二进制数的十进制等价物。它接受一个字符串参数，这是我们想要转换成十进制的二进制数。
参数必须是字符串，否则不同的数据类型会产生意外的结果。

**语法:**

```php
bindec(binary_string)
```

**参数:**该函数接受单个参数 *binary_string* ，表示要转换为十进制的二进制字符串。

**返回值:**返回二进制数*二进制 _ 字符串*的十进制值。

示例:

```php
Input : bindec('110011')
Output : 51

Input : bindec('000110011')
Output : 51

Input : bindec('111')
Output : 7

```

下面的程序说明了 PHP 中的 bindec()函数:

*   When ‘110011’ is passed as a parameter:

    ```php
    <?php

    echo bindec('110011');

    ?>      
    ```

    输出:

    ```php
    51
    ```

*   When ‘000110011’ is passed as a parameter:

    ```php
    <?php

    echo bindec('000110011');

    ?>      
    ```

    输出:

    ```php
    51
    ```

*   When ‘111’ is passed as a parameter:

    ```php
    <?php

    echo bindec('111');

    ?>
    ```

    输出:

    ```php
    7
    ```

**参考**:
T3】http://php.net/manual/en/function.bindec.php