# PHP | acos()函数

> 原文:[https://www.geeksforgeeks.org/php-acos-function/](https://www.geeksforgeeks.org/php-acos-function/)

三角学是数学的重要组成部分，PHP 的数学函数为我们提供了一些对涉及三角学的计算非常有用的函数。其中一个函数就是 acos()函数。PHP 中的 *acos()* 函数是用来求以弧度为单位的一个数的弧余弦。
我们已经讨论过 [PHP | cos()函数](https://www.geeksforgeeks.org/php-cos-function/)了。acos()函数是 cos()的互补函数。
在 acos()函数中传递的参数应该指定一个范围在-1 到 1 之间的数字。

**语法:**

```
*float* acos($value)
```

**参数:**该函数接受单个参数$值。它是您想要查找其弧余弦值的数字。此参数的值必须以弧度为单位。

**返回值:**返回一个浮点数，该浮点数是作为参数传递给它的数的弧余弦值。

示例:

```
Input : 0
Output : 1.5707963267949

Input : 1
Output : 0

Input : -1
Output : 3.1415926535898

Input : 2
Output : NaN

```

*   Passing 0 as a parameter:

    ```
    <?php

    echo (acos(0));

    ?>      
    ```

    输出:

    ```
    1.5707963267949
    ```

*   Passing 1 as a parameter:

    ```
    <?php

    echo (acos(1));

    ?>      
    ```

    输出:

    ```
    0
    ```

*   Passing -1 as a parameter:

    ```
    <?php

    echo (acos(-1));

    ?>      
    ```

    输出:

    ```
    3.1415926535898
    ```

*   Passing 2 as a parameter. As 2 is outside the range [-1,1], the function will return NaN :

    ```
    <?php

    echo (acos(2));

    ?>      
    ```

    输出:

    ```
    NaN
    ```

**参考**:
T3】http://php.net/manual/en/function.acos.php