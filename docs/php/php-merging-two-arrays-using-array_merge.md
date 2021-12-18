# PHP|使用 ARRAY_MERGE()

合并两个或多个数组

> Original: [https://www.geeksforgeeks.org/php-merging-two-arrays-using-array_merge/](https://www.geeksforgeeks.org/php-merging-two-arrays-using-array_merge/)

ARRAY_MERGE()是 PHP 中的一个内置函数，用于将两个或多个数组合并为一个数组。 此函数用于将两个或多个数组的元素或值合并为一个数组。 合并的方式是将一个数组的值追加到前一个数组的末尾。 该函数将以逗号分隔的数组列表作为需要合并的参数，并返回一个新数组，其中包含传入参数的数组合并值。

**语法：**

```php
*array* array_merge($array1, $array2, ......, $arrayn)
```

**参数：**ARRAY_MERGE()函数将逗号分隔的数组列表作为需要合并的参数，如语法所示。 共有 n 个数组(($array1，$array2，……。 ，$arrayn)在语法中用(‘，’)分隔。 我们可以在参数中传递任意数量的数组。

**返回值：**它返回一个新数组，其中所有传入参数的数组的元素都被合并，这样一个数组的值就会追加到前一个数组的末尾。

以下程序说明了 PHP 中 array_merge()函数的工作原理：

*   **Merging Two Simple Arrays**: When two more arrays are passed to the array_merge() function then the values of one array are appended at the end of the previous array. If two elements have the same string keys then the latter value will be overridden. The integer keys will be renumbered starting from zero. To merge two arrays, the array_merge() function can be executed in the following way:

    ```php
    <?php

    $my_array1 = array("size" => "big", 2,3 );
    $my_array2 = array("a", "b", "size" => "medium",
                            "shape" => "circle", 4);
    $res = array_merge($my_array1, $my_array2);

    print_r($res);

    ?>
    ```

    发帖主题：Re：Колибри0.7.8.0

    **注意：**如果输入数组包含相同的字符串键，则该键的后一个值将覆盖前一个值。

*   **传递带整数键的参数**：如果参数传递给 array_merge()函数，并且此数组参数的键是整数，则输出数组中的键将从 0 开始重新编号，并为下一个元素递增 1。下面的程序说明了这一点：

    ```php
    <?php

    $my_array = array(1 => "Geeks", 3=>"for", 2=>"Geeks");

    $res = array_merge($my_array);
    print_r($res);

    ?>
    ```

    **输出：**

    ```php
    Array
    (
        [0] => Geeks
        [1] => for
        [2] => Geeks     
    )
    ```

    ```php
    <?php

    $my_array1 = array(0 => 'zero_a', 2 => 'two_a', 3 => 'three_a');
    $my_array2 = array(1 => 'one_b', 3 => 'three_b', 4 => 'four_b');
    $res = array_merge($my_array1,$my_array2);
    print_r($res);

    ?>
    ```

    输出：

    ```php
    Array
    (
        [0] => zero_a
        [1] => two_a
        [2] => three_a
        [3] => one_b
        [4] => three_b
        [5] => four_b
    )

    ```