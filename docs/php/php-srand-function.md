# PHP|srand()函数

> Original: [https://www.geeksforgeeks.org/php-srand-function/](https://www.geeksforgeeks.org/php-srand-function/)

很多时候，在设计问题或算法时，我们需要生成随机数。 在文章[PHP|rand()函数](https://www.geeksforgeeks.org/php-rand-function/)中，我们已经研究了 PHP 中用于生成随机数的内置函数。 函数的作用是：生成随机数。 如果我们使用 rand()函数生成一个随机数序列，那么每次程序运行时，它都会一次又一次地创建相同的序列。 要解决此问题，可以使用 PHP 的另一个内置函数 srand()。

PHP 中的 srand()函数用于为随机数生成器 rand()设定种子。 函数的作用是：设置产生一系列伪随机整数的起点。 如果没有调用 srand()，则设置 rand()种子，就好像在程序启动时调用了 srand(1)一样。 Srand()函数为随机数生成器设定种子(Arg)种子，如果没有给出种子(Arg)，则给随机数生成器设定一个随机值。

**语法：**

```php
srand($seed)
```

**参数：**此函数接受单个参数*种子*。 它是一个可选参数，是整数类型。 它指定种子值。

**返回值：**此函数不返回任何值。

例如：

```php
Input : srand(time());
Output : 1793542495

Input : srand(5)
Output : 3

```

以下程序说明了 PHP 中的 srand()函数：

1.  When timestamp is used as the $seed value along with srand() function:

    ```php
    <?php

    srand(time());

    echo(rand());

    ?>
    ```

    产出：

    ```php
    1793542495
    ```

2.  When a user-defined seed value is passed as an argument with srand() function:

    ```php
    <?php

    srand(5); 

    echo(rand(1, 10)); 

    ?>
    ```

    产出：

    ```php
    3
    ```

**重要注意事项：**

*   Srand()函数可用于生成随机数。
*   Srand()函数不会创建与 rand()函数相同的随机数序列。
*   它没有返回值。

**引用**：
[http://php.net/manual/en/function.srand.php](http://php.net/manual/en/function.srand.php)