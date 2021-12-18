# PHP|sinh()函数

> Original: [https://www.geeksforgeeks.org/php-sinh-function/](https://www.geeksforgeeks.org/php-sinh-function/)

*sinh()*函数是 PHP 中的内置函数，用于查找角度的双曲正弦。
任意自变量*Arg*的双曲正弦被定义为，

(exp(Arg)-ex(-arg))/2

其中，exp()是指数函数，返回的 e 是传递给它的参数的幂。 例如 exp(2)=e^2。

**语法：**

```php
*float* sinh($value)
```

**参数：**此函数接受单个参数$VALUE。 它是您要查找其双曲正弦值的数字。 此参数的值必须以弧度为单位。

**返回值：**它返回一个浮点数，它是作为参数传递给它的数字的双曲正弦值。

例如：

```php
Input : sinh(3) 
Output : 10.01787492741

Input : sinh(-3)
Output : -10.01787492741

Input : sinh(M_PI)
Output : 11.548739357258

Input : sinh(0) 
Output : 0

```

下面的程序使用不同的$value 值来说明 PHP 中的 sinh()函数：

*   Passing 3 as a parameter:

    ```php
    <?php

    echo (sinh(3));

    ?>      
    ```

    产出：

    ```php
    10.01787492741
    ```

*   Passing -3 as a parameter:

    ```php
    <?php

    echo (sinh(-3));

    ?>      
    ```

    产出：

    ```php
    -10.01787492741
    ```

*   When (M_PI) is passed as a parameter, M_PI is a constant in PHP whose value is 3.1415926535898:

    ```php
    <?php

    echo (sinh(M_PI));

    ?>      
    ```

    产出：

    ```php
    11.548739357258
    ```

*   Passing 0 as a parameter:

    ```php
    <?php

    echo (sinh(0));

    ?>      
    ```

    产出：

    ```php
    0
    ```

**参考**：
[http://php.net/manual/en/function.sinh.php](http://php.net/manual/en/function.sinh.php)