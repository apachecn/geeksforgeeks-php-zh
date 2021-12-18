# PHP|uasort()函数

> Original: [https://www.geeksforgeeks.org/php-uasort-function/](https://www.geeksforgeeks.org/php-uasort-function/)

Uasort()函数是 PHP 中的一个内置函数，用于对数组进行排序，以便数组索引使用用户定义的比较函数保持其与数组元素相关联的相关性。

**语法：**

```
*boolean* uasort(array_name, user_defined_function);

```

**参数：**此函数接受两个参数，说明如下：

1.  **ARRAY_NAME**：该参数表示需要排序的数组。
2.  **USER_DEFINED_Function**：这是一个比较器函数，用于比较值和对数组排序。 此函数返回三种类型的值，如下所述：
    *   当 a=b 时返回 0
    *   当 a>b 且我们想要按升序对输入数组排序时，它返回 1，否则，如果我们想要按降序对输入数组排序，它将返回-1。
    *   当 a

****返回值：**它返回一个布尔值，即成功时返回 TRUE，失败时返回 FALSE。**

**例如：**

```
Input: array
       (
            "a" => 4,
            "b" => 2,
            "g" => 8,
            "d" => 6,
            "e" => 1,
            "f" => 9
       )
Output: Array 
        ( 
            [e] => 1 
            [b] => 2 
            [a] => 4 
            [d] => 6 
            [g] => 8 
            [f] => 9 
        ) 
```

**以下程序说明了 PHP 中的 uasort()函数：**

*   ****Sorting in ascending order**: To sort the input array in ascending order, in the comparator function we will return 1 when a>b or -1 when a<b. Below program illustrates this:

    ```
    <?php
    // PHP program to sort in ascending
    // order using uasort() function

    // user_defined comparator function
    function sorting($a,$b)
    {
        if ($a==$b) return 0;
            return ($a<$b)?-1:1;
    }

    // input array  
    $arr=array("a"=>4,"b"=>2,"g"=>8,"d"=>6,"e"=>1,"f"=>9);

    uasort($arr,"sorting");

    // printing sorted array.
    print_r($arr);

    ?>
    ```

    产出：

    ```
    Array
    (
        [e] => 1
        [b] => 2
        [a] => 4
        [d] => 6
        [g] => 8
        [f] => 9
    )

    ```** 
*   ****Sorting in descending order**: To sort the input array in descending order, in the comparator function we will return -1 when a>b or 1 when a<b. Below program illustrates this:

    ```
    <?php
    // PHP program to sort in descending
    // order using uasort() function

    // user_defined comparator function
    function sorting($a, $b) 
    {
        if ($a == $b) return 0;
            return ($a > $b) ? -1 : 1;
    }

    // input array
    $input = array("d"=>"R", "a"=>"G", "b"=>"X", "f"=>"Z" );

    uasort($input, "sorting");

    // printing sorted array.
    print_r($input);

    ?>
    ```

    产出：

    ```
    Array
    (
        [f] => Z
        [b] => X
        [d] => R
        [a] => G
    )

    ```** 

****引用：**
[http://php.net/manual/en/function.uasort.php](http://php.net/manual/en/function.uasort.php)**