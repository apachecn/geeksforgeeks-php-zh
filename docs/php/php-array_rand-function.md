# PHP | array_rand()函数

> 原文:[https://www.geeksforgeeks.org/php-array_rand-function/](https://www.geeksforgeeks.org/php-array_rand-function/)

PHP 的这个内置函数用于从数组中获取随机数量的元素。元素是一个键，可以返回一个或多个键。实际上，这没有那么有用，因为该函数使用不适合加密目的的伪随机数生成器。

**语法**:

```
array_rand($array, $num)
```

**参数:**该函数只接受两个参数，描述如下:

1.  **$array(必选):**这是必选参数，指的是原始输入数组。
2.  **$num(可选):**此参数指需要返回的随机数个数。该值必须大于或等于 1，否则将引发 E_WARNING。

**返回值:**该函数从数组中返回随机生成的值。返回的元素数量取决于分配给函数的$num 的值。

示例:

```
Input : 
$array = ("ram"=>"20", "krishna"=>"42", "aakash"=>"15")
$num = 2
Output :
Array
(
    [0] => ram
    [1] => aakash
)

Input :
$array = ("ram"=>"20", "krishna"=>"42", "aakash"=>"15")
Output : krishna

```

下面的程序说明了 PHP 中的 array_rand()函数:

*   In the below program we have passed our second parameter that specifies the number of elements to be returned.

    ```
    <?php
    // PHP function to illustrate the use 
    // of array_rand()
    $array = array("ram"=>"20", "krishna"=>"42", 
                                "aakash"=>"15");
    $num = 2;
    print_r(array_rand($array, $num));
    ?>
    ```

    输出:

    ```
    Array
    (
        [0] => ram
        [1] => krishna
    )

    ```

*   Now let’s see what will happen if we don’t pass the second parameter.

    ```
    <?php
    // PHP function to illustrate the 
    // use of array_rand()
    $array = array("ram"=>"20", "krishna"=>"42",
                                "aakash"=>"15");
    print_r(array_rand($array));
    ?>
    ```

    输出:

    ```
    aakash

    ```

**参考**:
T3】http://php.net/manual/en/function.array-rand.php