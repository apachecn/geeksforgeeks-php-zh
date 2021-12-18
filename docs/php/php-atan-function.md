# PHP | atan()函数

> 原文:[https://www.geeksforgeeks.org/php-atan-function/](https://www.geeksforgeeks.org/php-atan-function/)

三角学是数学的重要组成部分，PHP 的数学函数为我们提供了一些对涉及三角学的计算非常有用的函数。其中一个函数就是 atan()函数。
PHP 中的 *atan()* 函数用于查找传递给它的参数的反正切，该参数的数值在-Pi/2 和 Pi/2 弧度之间。
我们已经讨论过 [PHP | tan()函数](https://www.geeksforgeeks.org/php-tan-function/)。atan()函数是 tan()的互补函数。

**语法:**

```php
*float* atan($value)
```

**参数:**该函数接受单个参数$值。这是您要查找其反正切值的数字。此参数的值必须以弧度为单位。

**返回值:**返回一个浮点数，该浮点数是作为参数传递给它的数的反正切值。

示例:

```php
Input : atan(0.50)  
Output : 0.46364760900081

Input : atan(-0.50) 
Output : -0.46364760900081

Input : atan(5)
Output : 1.373400766945

Input : atan(100) 
Output : 1.5607966601082

```

下面用不同的$value 值说明 PHP 中的 atan()函数:

*   Passing 0.50 as a parameter:

    ```php
    <?php

    echo (atan(0.50));

    ?>    
    ```

    输出:

    ```php
    0.46364760900081
    ```

*   Passing -0.50 as a parameter:

    ```php
    <?php

    echo (atan(-0.50));

    ?>      
    ```

    输出:

    ```php
    -0.46364760900081
    ```

*   Passing 5 as a parameter:

    ```php
    <?php

    echo (atan(5));

    ?>      
    ```

    输出:

    ```php
    1.373400766945
    ```

*   Passing 100 as a parameter:

    ```php
    <?php

    echo (atan(100));

    ?>      
    ```

    输出:

    ```php
    1.5607966601082
    ```

**参考**:
T3】http://php.net/manual/en/function.atan.php