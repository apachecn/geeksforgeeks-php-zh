# 如何使用 php 序列化()和反序列化()函数

> 原文:[https://www . geesforgeks . org/how-用法-PHP-serialize-and-unserialize-function/](https://www.geeksforgeeks.org/how-to-use-php-serialize-and-unserialize-function/)

在 PHP 中，复杂的数据无法传输或存储。如果您想在单个脚本之外连续执行一组复杂的数据，那么这个 serialize()和 unserialize()函数可以方便地处理这些复杂的数据结构。serialize()函数只是为一个复杂的数据结构提供了一个兼容的形状，PHP 可以处理该数据，之后您可以使用 unserialize()函数来反转工作。

大多数情况下，我们需要将一个复杂的数组存储在数据库或 PHP 的文件中。我们中的一些人肯定已经搜索了一些内置函数来完成这个任务。复杂数组是包含多个数据类型或数组元素的数组。但是，我们已经有一个方便的解决方案来处理这种情况。

**Serialize()函数:**Serialize()是一个内置函数 PHP，用于序列化给定的数组。serialize()函数接受单个参数，即我们要序列化的数据，并返回一个序列化的字符串。

*   **语法:**

    ```php
    serialize( $values_in_form_of_array )
    ```

*   下面的程序说明了 Serialize()函数。
    **程序:**

    ```php
    <?php 

    // Complex array 
    $myvar = array( 
        'hello', 
        42, 
        array(1, 'two'), 
        'apple'
    ); 

    // Convert to a string 
    $string = serialize($myvar); 

    // Printing the serialized data 
    echo $string; 

    ?> 
    ```

*   **输出:**

    ```php
    a:4:{i:0;s:5:"hello";i:1;i:42;i:2;a:2:{i:
    0;i:1;i:1;s:3:"two";}i:3;s:5:"apple";}
    ```

**Unserialize()函数:**Unserialize()是一个内置函数 php，用于对给定的序列化数组进行非序列化，以返回复杂数组$myvar 的原始值。

*   **语法:**

    ```php
    unserialize( $serialized_array )
    ```

*   下面的程序说明了序列化()和非序列化()函数:
    **程序:**

    ```php
    <?php 

    // Complex array 
    $myvar = array( 
        'hello', 
        42, 
        array(1, 'two'), 
        'apple'
    ); 

    // Serialize the above data 
    $string = serialize($myvar); 

    // Unserializing the data in $string 
    $newvar = unserialize($string); 

    // Printing the unserialized data 
    print_r($newvar); 

    ?> 
    ```

*   **输出:**

    ```php
    Array
    (
        [0] => hello
        [1] => 42
        [2] => Array
            (
                [0] => 1
                [1] => two
            )

        [3] => apple
    )

    ```

**注:**更多深度知识可以查看 [PHP |序列化数据](https://www.geeksforgeeks.org/php-serializing-data/)文章。