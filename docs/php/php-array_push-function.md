# PHP | array_push()函数

> 原文:[https://www.geeksforgeeks.org/php-array_push-function/](https://www.geeksforgeeks.org/php-array_push-function/)

PHP 的这个内置函数用于将新元素推入数组。我们可以将一个或多个元素推入数组，这些元素被插入到数组的末尾，并且由于将元素推入数组，数组的长度也会随着推入数组的元素数量而增加。

**语法**:

```php
array_push($array, $val1, $val2, $val3....)
```

**参数:**
该函数可以取多个参数，具体取决于我们想要推入数组的元素数量。我们可以将参数分为两类，如下所示:

1.  **$array:** 这个参数是指我们要操作的原始数组。
2.  **值列表:**这个参数指的是我们要推入数组的用逗号分隔的元素列表。在上面的语法中，要推送的值列表是$val1、$val2、$val3…

**返回值:**该函数返回修改后的数组，所有元素被推到数组末尾。

**注意:**如果数组中有一个键、值对，那么该方法将总是给推送的值添加一个数字键。

示例:

```php
Input : $array = (1=>"ram", 2=>"krishna", 3=>"aakash")
        $val1 = "rohan", $val2 = "rajeeb", $val3 = "saniya"
Output : 
Array
(
    [1] => ram
    [2] => krishna
    [3] => aakash
    [4] => rohan
    [5] => rajeeb
    [6] => saniya
)

Input : $array = ("ram", "krishna", "aakash");
        $val1 = "rohan", $val2 = "rajeeb", $val3 = "saniya"
Output :
Array
(
    [0] => ram
    [1] => krishna
    [2] => aakash
    [3] => rohan
    [4] => rajeeb
    [5] => saniya
)

```

下面的程序说明了 PHP 中的 array_push()函数:

*   In the below program the array_push() function is used to push new elements in an array with no keys.

    ```php
    <?php
    // PHP code to illustrate the use of array_push()

    // Input array
    $array = array("ram", "krishna", "aakash");

    // elements to push
    $a1 = "rohan";
    $a2 = "rajeeb";
    $a3 = "saniya";

    // array after pushing new elements
    print_r(array_push($array, $a1, $a2, $a3));
    ?>
    ```

    输出:

    ```php
    Array
    (
        [0] => ram
        [1] => krishna
        [2] => aakash
        [3] => rohan
        [4] => rajeeb
        [5] => saniya
    )

    ```

*   In the below program, we will understand how the array_push() function works with an array having a already defined key_value pair.

    ```php
    <?php
    // PHP code to illustrate the use of array_push()

    // Input Array
    $array = array(1=>"ram", 2=>"krishna", 3=>"aakash");

    // Elements to push
    $a1 = "rohan";
    $a2 = "rajeeb";
    $a3 = "saniya";

    // Array after pushing new elements
    print_r(array_push($array, $a1, $a2, $a3));
    ?>
    ```

    输出:

    ```php
    Array
    (
        [1] => ram
        [2] => krishna
        [3] => aakash
        [4] => rohan
        [5] => rajeeb
        [6] => saniya
    )

    ```

**参考**:
T3】http://php.net/manual/en/function.array-push.php