# PHP|intdiv()函数

> Original: [https://www.geeksforgeeks.org/php-intdiv-function/](https://www.geeksforgeeks.org/php-intdiv-function/)

Intdiv 代表整数除法。 此函数返回给定被除数和除数的除法的整数商。 此函数在内部删除被除数中的余数，使其可被除数整除，并在除法后返回商。

**语法：**

```php
*int* intdiv($dividend, $divisor)

```

**参数**：该函数有两个参数，如下所示：

*   $DYARY：这个带符号的整数参数指的是要除法的数字。
*   $ditor：这个带符号的整数参数引用要用作除数的数字。

**返回类型**：此函数返回计算出的商。

例如：

```php
Input :  $dividend = 5, $divisor = 2
Output : 2

Input : $dividend = -11, $divisor = 2
Output : -5        

```

**异常/错误：**：函数在以下情况下引发异常：

*   如果我们将除数作为 0 传递，则函数将引发 DivisionByZeroError 异常。
*   If we pass PHP_INT_MIN as the dividend and -1 as the divisor, then an ArithmeticError exception is thrown.

    下面的程序演示了 intdiv 在 PHP 中的工作方式：

    ```php
    <?php

    // PHP code to illustrate the working 
    // of intdiv() Functions 

    $dividend = 19;
    $divisor = 3; 

    echo intdiv($dividend, $divisor);

    ?>
    ```

    产出：

    ```php
    6

    ```

    到目前为止，很多人可能会认为这个函数等同于

    ```php
    floor($dividend/$divisor)
    ```

    但这个例子将详细说明不同之处。

    ```php
    <?php

    // PHP code to differentiate between 
    // intdiv() and floor() 

    $dividend = -19;
    $divisor = 3; 

    echo intdiv($dividend, $divisor) ."\n". 
                 floor($dividend/ $divisor);

    ?>
    ```

    产出：

    ```php
    -6
    -7

    ```

    **需要注意的重要事项**：

    *   Intdiv()函数返回整数除法的商。
    *   该函数可能会引发异常，因此开发人员必须处理边缘情况。
    *   该函数不等同于应用于浮点数除法或‘/’的 FLOOR 函数。

    **参考**：
    [http://php.net/manual/en/function.intdiv.php](http://php.net/manual/en/function.intdiv.php)