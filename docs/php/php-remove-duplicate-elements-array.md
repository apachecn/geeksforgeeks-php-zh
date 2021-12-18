# PHP|从数组

中删除重复元素

> Original: [https://www.geeksforgeeks.org/php-remove-duplicate-elements-array/](https://www.geeksforgeeks.org/php-remove-duplicate-elements-array/)

您将看到一个 n 元素数组，您必须在不使用 PHP 中任何循环的情况下删除重复的值，然后打印该数组。

示例：

```php
Input : array[] = {2, 3, 1, 6, 1, 6, 2, 3}
Output : array (
                [6] => 2
                [7] => 3
                [4] => 1
                [5] => 6
               )

Input : array[] = {4, 2, 7, 3, 2, 7, 3}
Output : array (
                [0] => 4
                [4] => 2
                [5] => 7
                [6] => 3 
               )

```

在[C](https://www.geeksforgeeks.org/c-programming-language/)/[Java](https://www.geeksforgeeks.org/java/)中，我们必须遍历数组，并且对于每个元素，您必须检查是否存在重复的元素。 但是 PHP 提供了一个内置函数(array_flip())，通过使用该函数，我们可以在不使用循环的情况下删除重复的元素。

**[array_flip()](https://www.geeksforgeeks.org/php-array_flip-function/)**以反转顺序返回数组，即数组中的键变成值，数组中的值变成键。

*注意，数组的值需要是有效的键，即它们需要是整数或字符串。 如果值的类型错误，则会发出警告，并且有问题的键/值对不会包含在结果中。*

**注意：**如果某个值出现多次，将使用最新的密钥作为其值，其他所有密钥都将丢失。 另外，由于[array_flip()](https://www.geeksforgeeks.org/php-array_flip-function/)返回具有保留键的数组，我们将使用[array_value()](https://www.geeksforgeeks.org/php-array_values-function/)，它将重新排序键。

**方法：**其思想是使用 array_flip()函数的这个属性，如果值多次出现，则选择最新的键作为其值。 我们将使用 array_flip()函数两次来删除重复值。 在第一次使用 array_flip()函数时，它将返回一个数组，其中包含与删除的重复项交换的键和值。 第二次使用时，它会再次将其重新排序为原始配置。

以下是上述想法的实施情况：

```php
<?php
    // define array
    $a = array(1, 5, 2, 5, 1, 3, 2, 4, 5);

    // print original array
    echo "Original Array : \n";
    print_r($a);

    // remove duplicate values by using 
    // flipping keys and values
    $a = array_flip($a);

    // restore the array elements by again 
    // flipping keys and values.
    $a = array_flip($a);

    // re-order the array keys
    $a= array_values($a);

    // print updated array
    echo "\nUpdated Array : \n ";
    print_r($a);
?>
```

帖子主题：Re：Колибри