# PHP|EXPLODE()函数

> Original: [https://www.geeksforgeeks.org/php-explode-function/](https://www.geeksforgeeks.org/php-explode-function/)

EXPLIDE()是 PHP 中的一个内置函数，用于将一个字符串拆分成不同的字符串。 函数的作用是：根据字符串分隔符拆分字符串，即在出现分隔符的任何位置拆分字符串。 此函数返回一个数组，其中包含通过拆分原始字符串形成的字符串。
**语法：**和

```php
*array* explode(separator, OriginalString, NoOfElements)
```

**参数：**分解函数接受三个参数，其中两个是必选的，一个是可选的。 下面描述了所有这三个参数

1.  **分隔符：**此字符指定字符串将拆分的一个或多个临界点，即每当在字符串中找到此字符时，它就象征着数组中一个元素的结束和另一个元素的开始。
2.  **OriginalString：**要在数组中拆分的输入字符串。
3.  **NoOfElements：**这是可选的。 它用于指定数组的元素数。 此参数可以是任意整数(正、负或零)
    *   **正(N)：**当此参数以正值传递时，表示数组将包含此数量的元素。 如果相对于分隔符分隔后的元素数量大于此值，则前 N-1 个元素保持不变，最后一个元素是整个剩余字符串。
    *   **负(N)：**如果将负值作为参数传递，则数组的最后 N 个元素将被修剪掉，数组的其余部分将作为单个数组返回。
    *   **零：**如果此参数为零，则返回的数组将只有一个元素，即整个字符串。

**返回类型**：EXPLODE()函数的返回类型为字符串数组。
示例：

```php
Input : explode(" ","Geeks for Geeks")
Output : Array
        (
            [0] => Geeks
            [1] => for
            [2] => Geeks
        )
```

下面的程序说明了在 PHP 中 EXPLODE()的工作方式：

## PHP

```php
<?php

    // original string
    $OriginalString = "Hello, How can we help you?";

    // Without optional parameter NoOfElements
    print_r(explode(" ",$OriginalString));
    // with positive NoOfElements
    print_r(explode(" ",$OriginalString,3));
    // with negative NoOfElements
    print_r(explode(" ",$OriginalString,-1));

?>
```

输出：0

```php
Array
(
    [0] => Hello,
    [1] => How
    [2] => can
    [3] => we
    [4] => help
    [5] => you?
)
Array
(
    [0] => Hello,
    [1] => How
    [2] => can we help you?
)
Array
(
    [0] => Hello,
    [1] => How
    [2] => can
    [3] => we
    [4] => help
)
```

**参考**：[http://php.net/manual/en/function.explode.php](http://php.net/manual/en/function.explode.php)