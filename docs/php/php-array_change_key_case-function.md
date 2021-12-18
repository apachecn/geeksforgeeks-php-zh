# PHP | array_change_key_case()函数

> 原文:[https://www . geesforgeks . org/PHP-array _ change _ key _ case-function/](https://www.geeksforgeeks.org/php-array_change_key_case-function/)

array_change_key_case()函数是 PHP 中的一个内置函数，用于将给定数组中所有键的大小写改为小写或大写。

**语法:**

```php
*array* array_change_key_case(in_array, convert_case)
```

**参数**:该功能接受两个参数，其中一个是强制的，另一个是可选的。这两个参数描述如下:

1.  **in_array(必选):**此参数指的是需要更改键大小写的数组。
2.  **convert_case(可选):**这是一个可选参数，指的是我们需要转换数组的键的‘case’。这可以取两个值，或者是大写，或者是小写。大小写值决定大写字母，大小写决定小写字母。如果没有通过 *convert_case* 参数，则取默认值 CASE _ LOWER。

**注意:**如果第二个参数被忽略，那么默认情况下数组的键将被转换为小写。

**返回类型**:该函数返回一个改变了键大小写的数组，可以是小写，也可以是大写。

现在让我们看看一些程序，以更好地理解 array_change_key_case()函数的工作原理。

*   Below program converts the case of keys to uppercase:

    ```php
    <?php

    // PHP code to illustrate array_change_key_case()
    // Both the parameters are passed
    function change_case($in_array){
        return(array_change_key_case($in_array, CASE_UPPER));
    }

    // Driver Code
    $array = array("Aakash" => 90, "RagHav" => 80, 
                   "SiTa" => 95, "rohan" => 85, "RISHAV" => 70);
    print_r(change_case($array));

    ?>
    ```

    输出:

    ```php
    Array
    (
        [AAKASH] => 90
        [RAGHAV] => 80
        [SITA] => 95
        [ROHAN] => 85
        [RISHAV] => 70
    )

    ```

*   If we ignore the second parameter *convert_case* in the function array_change_key_case() then the keys will be converted to lowercase. Below program illustrates this:

    ```php
    <?php

    // PHP code to illustrate array_change_key_case()
    // Second parameter is ignored
    function change_case($in_array){
        return(array_change_key_case($in_array));
    }

    // Driver Code
    $array = array("Aakash" => 90, "RagHav" => 80, 
                   "SiTa" => 95, "rohan" => 85, "RISHAV" => 70);
    print_r(change_case($array));

    ?>
    ```

    输出:

    ```php
    Array
    (
        [aakash] => 90
        [raghav] => 80
        [sita] => 95
        [rohan] => 85
        [rishav] => 70
    )

    ```

*   If we don’t pass an array to the function then PHP_Warning is popped up, but the program works and No Output is generated. Below program illustrates this

    ```php
    <?php

    // PHP code to illustrate array_change_key_case()
    // NO parameter is passed
    function change_case($in_array){
        return(array_change_key_case());
    }

    // Driver Code
    $array = array("Aakash" => 90, "RagHav" => 80, 
                   "SiTa" => 95, "rohan" => 85, "RISHAV" => 70);
    print_r(change_case($array));

    ?>
    ```

    输出:

    ```php
    No Output

    ```

    警告:

    ```php
    PHP Warning:  array_change_key_case() expects at least 1 parameter, 
    0 given in /home/7d540b2d77cbbfa46af4fb8798fb5e79.php on line 5
    ```