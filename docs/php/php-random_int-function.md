# PHP|Random_int()函数

> Original: [https://www.geeksforgeeks.org/php-random_int-function/](https://www.geeksforgeeks.org/php-random_int-function/)

**Random_int()**是 PHP 中的内置函数。 主要功能是生成密码安全的伪随机整数值。 当无偏结果在临界条件下出现时，则使用生成的密码随机整数。

此函数中使用的不同随机性来源如下：

*   **窗口：**使用的 CryptGenRandom()函数。
*   **Linux：**要使用的 getRandom(2)系统调用函数。

**语法：**

```
int random_int ( $min, $max )

```

**参数：**

*   **$min：**返回**最低值**，等于或大于 PHP_INT_MIN。
*   **$max：**返回**最高值**，该值小于或等于 PHP_INT_MAX。

**返回值：**一个加密安全的随机整数，取值范围为 min 到 max(含 min 和 max)。

例如：

```
Input : min= 10, max=10000
Output : int(5183)

Input : min= -244441, max= 1
Output : int(-60209)

```

下面的程序演示了 PHP 中的 Random_int()函数。
**程序 1：**

```
<?php
// PHP program to demonstrate
// the random_int() function 

// given min and max range
var_dump(random_int(1, 5555555));
var_dump(random_int(-1, 100000));
var_dump(random_int(9, 10));

?>
```

输出

```
int(835427)
int(86695)
int(10)

```

下面的程序演示了 PHP 中的 Random_int()函数。

**程序 2：**
当写入无效范围时，则会出现运行时错误。

```
<?php
// PHP program to demonstrate
// the random_int() function 

// given min and max range
// Not valid range
$t = (random_int(99, 11));

// Print result
echo "(int)", $t;
?>
```

输出

```
Runtime Error

```

**异常错误：**

*   无效参数提供**TypeError**。
*   无效的字节长度给出**错误**。
*   如果未找到随机性来源，则将抛出异常。

**引用：**
[http://php.net/manual/en/function.random-int.php](http://php.net/manual/en/function.random-int.php)