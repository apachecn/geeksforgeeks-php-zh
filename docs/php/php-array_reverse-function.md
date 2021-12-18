# PHP | array_reverse()函数

> 原文:[https://www.geeksforgeeks.org/php-array_reverse-function/](https://www.geeksforgeeks.org/php-array_reverse-function/)

PHP 的这个内置函数用于反转包括嵌套数组在内的数组元素。此外，我们可以根据用户的选择保留关键元素。这个函数接受一个数组作为参数，并以相反的顺序返回包含元素的数组。

**语法**:

```php
*array* array_reverse($array, $key_preserve)
```

**参数:**
该函数采用两个参数，描述如下:

1.  **$array(必选):**此参数指的是原始数组。
2.  **$key_preserve(可选):**这是一个可选参数，可以设置为 TRUE 或 FALSE，它指的是数组的键的保存。默认情况下，该参数的值为假。

**返回值:**该函数返回传入参数的数组，元素的顺序相反。

示例:

```php
Input : $array = (2, 4, 5, 10, 100)
Output : 
Array
(
    [0] => 100
    [1] => 10
    [2] => 5
    [3] => 4
    [4] => 2
)

Input :
Array
(
    [0] => ram
    [1] => aakash
    [2] => saran
    [3] => mohan
)
Output :
Array
(
    [3] => mohan
    [2] => saran
    [1] => aakash
    [0] => ram
)

```

下面的程序说明了 PHP 中的 array_reverse()函数:

1.  This program reverses an array taking the $key_preserve as FALSE by default. This don’t presere the keys.

    ```php
    <?php

    // PHP function to illustrate the use of array_reverse()
    function Reverse($array)
    {
        return(array_reverse($array));
    }

    $array = array("ram", "aakash", "saran", "mohan");

    echo "Before:\n";
    print_r($array);

    echo "\nAfter:\n";
    print_r(Reverse($array));

    ?>
    ```

    输出:

    ```php
    Before:
    Array
    (
        [0] => ram
        [1] => aakash
        [2] => saran
        [3] => mohan
    )

    After:
    Array
    (
        [0] => mohan
        [1] => saran
        [2] => aakash
        [3] => ram
    )
    ```

2.  Let’s see what happens when we pass the key_preserve parameter as TRUE. This preserve the keys.

    ```php
    <?php

    // PHP function to illustrate the use of array_reverse()
    function Reverse($array)
    {
        return(array_reverse($array, true));
    }

    $array = array("ram", "aakash", "saran", "mohan");

    echo "Before:\n";
    print_r($array);

    echo "\nAfter:\n";
    print_r(Reverse($array));

    ?>
    ```

    输出:

    ```php
    Before:
    Array
    (
        [0] => ram
        [1] => aakash
        [2] => saran
        [3] => mohan
    )

    After:
    Array
    (
        [3] => mohan
        [2] => saran
        [1] => aakash
        [0] => ram
    )

    ```

**参考**:
T3】http://php.net/manual/en/function.array-reverse.php