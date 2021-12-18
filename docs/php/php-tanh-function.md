# PHP|tanh()函数

> Original: [https://www.geeksforgeeks.org/php-tanh-function/](https://www.geeksforgeeks.org/php-tanh-function/)

*tanh()*函数是 PHP 中的一个内置函数，用于查找作为参数传递给它的角度的双曲正切。 任意自变量*Arg*的双曲正切定义为，

正弦(Arg)/cosh(Arg)

其中，[sinh()](https://www.geeksforgeeks.org/php-sinh-function/)是双曲正弦函数，[cosh()](https://www.geeksforgeeks.org/php-cosh-function/)是双曲余弦函数。

**语法：**

```php
*float* tanh($value)
```

**参数：**此函数接受单个参数$VALUE。 它是您要查找其双曲正切值的数字。 此参数的值必须以弧度为单位。

**返回值：**它返回一个浮点数，它是作为参数传递给它的数的双曲正切值。

例如：

```php
Input : tanh(0.50)  
Output : 0.46211715726001

Input : tanh(-0.50) 
Output : -0.46211715726001

Input : tanh(5)
Output : 0.9999092042626

Input : tanh(M_PI_4) 
Output : 0.65579420263267

```

下面的程序使用不同的$value 值来说明 PHP 中的 tanh()函数：

*   Passing 0.50 as a parameter:

    ```php
    <?php

    echo (tanh(0.50));

    ?>      
    ```

    产出：

    ```php
    0.46211715726001
    ```

*   Passing -0.50 as a parameter:

    ```php
    <?php

    echo (tanh(-0.50));

    ?>      
    ```

    产出：

    ```php
    -0.46211715726001
    ```

*   Passing 5 as a parameter:

    ```php
    <?php

    echo (tanh(5));

    ?>      
    ```

    产出：

    ```php
    0.9999092042626
    ```

*   When (M_PI_4) is passed as a parameter, M_PI is a constant in PHP whose value is 0.78539816339744830962 :

    ```php
    <?php

    echo (tanh(M_PI_4));

    ?>      
    ```

    产出：

    ```php
    0.65579420263267
    ```

**参考**：
[http://php.net/manual/en/function.tanh.php](http://php.net/manual/en/function.tanh.php)