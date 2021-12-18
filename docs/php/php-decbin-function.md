# PHP|decbin()函数

> Original: [https://www.geeksforgeeks.org/php-decbin-function/](https://www.geeksforgeeks.org/php-decbin-function/)

在处理数字时，很多时候我们需要转换数字的基数，最常用的转换之一是十进制到二进制的转换。 PHP 为我们提供了一个内置函数*decbin()*。PHP 中的 decbin()函数用于返回包含给定十进制数参数的二进制表示形式的字符串。
decbin 代表十进制到二进制。

**语法：**

```php
*string* decbin(value)
```

**参数：**此函数接受单个参数*值*。 它是要转换为二进制表示的十进制数。

**返回值：**它返回一个字符串，该字符串表示作为参数传递给函数的十进制数的二进制值。

例如：

```php
Input : decbin(12)
Output : 1100

Input : decbin(26)
Output : 11010

Input : decbin(2147483647)
Output : 1111111111111111111111111111111 (31 1's)

```

下面的程序演示了 PHP 中的 decbin()函数：

*   Passing 12 as a parameter

    ```php
    <?php

    echo decbin(12);

    ?>    
    ```

    产出：

    ```php
    1100
    ```

*   Passing 26 as a parameter:

    ```php
    <?php

    echo decbin(26);

    ?>   
    ```

    产出：

    ```php
    11010
    ```

*   When the largest signed integer is passed as a parameter:

    ```php
    <?php

    echo decbin(2147483647);

    ?>      
    ```

    产出：

    ```php
     1111111111111111111111111111111  
    ```

**参考**：
[http://php.net/manual/en/function.decbin.php](http://php.net/manual/en/function.decbin.php)