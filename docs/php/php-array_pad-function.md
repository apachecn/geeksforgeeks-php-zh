# PHP | array_pad()函数

> 原文:[https://www.geeksforgeeks.org/php-array_pad-function/](https://www.geeksforgeeks.org/php-array_pad-function/)

array_pad()是 PHP 中的内置函数，用于将一个值固定次数地填充到一个数组中。这个函数在数组的前面或后面插入指定次数的元素。

**语法:**

```
*array* array_pad($input_array, $input_size, $values)
```

**参数:**该功能接受三个参数，所有这些都是必须提供的。

1.  **$input_array(必选):**指要对其执行操作的数组，或者需要向其添加元素的数组。
2.  **$total_size(强制):**指要返回的新数组的总大小。
    *   如果值为正，元素将被添加到数组的末尾。
    *   如果该值为负，则在数组的开头添加元素。
3.  **$values(强制):**指进行填充的值。只有当 *$total_size* 大于 input_array 的大小时，填充才会发生。

**返回值:**函数返回填充到$total_size 大小的数组副本。如果$total_size 的绝对值小于或等于数组的长度，则不发生填充。一次最多可以添加 1048576 个元素。

示例:

```
Input : array = ("one", "two", "three", "four", "five")
        $total_size  = 7 , $value = "six"
Output : 
Array
(
    [0] => one
    [1] => two
    [2] => three
    [3] => four
    [4] => five
    [5] => six
    [6] => six
)

Input : array = ("one", "two", "three", "four", "five")
        $total_size  = -7 , $value = "six"
Output : 
Array
(
    [0] => six
    [1] => six
    [2] => one
    [3] => two
    [4] => three
    [5] => four
    [6] => five
)

```

下面的程序解释了 array_pad()函数的工作原理:

1.  Padding elements at end of the array when the $total_size is positive:

    ```
    <?php
    // PHP function to illustrate the use of array_pad()
    function Padding($array, $string)
    {
        $result = array_pad($array, 7, $string);
        return($result);
    }

    $array = array("one", "two", "three", "four", "five");
    $string = "six";
    print_r(Padding($array, $string));
    ?>
    ```

    输出:

    ```
    Array
    (
        [0] => one
        [1] => two
        [2] => three
        [3] => four
        [4] => five
        [5] => six
        [6] => six
    )

    ```

2.  Padding elements at start of the array when the $total_size is negative:

    ```
    <?php
    // PHP function to illustrate the use of array_pad()
    function Padding($array, $string)
    {
        $result = array_pad($array, -7, $string);
        return($result);
    }

    $array = array("one", "two", "three", "four", "five");
    $string = "six";
    print_r(Padding($array, $string));
    ?>
    ```

    输出:

    ```
    Array
    (
        [0] => six
        [1] => six
        [2] => one
        [3] => two
        [4] => three
        [5] => four
        [6] => five
    )

    ```