# PHP | array_replace()函数

> 原文:[https://www.geeksforgeeks.org/php-array_replace-function/](https://www.geeksforgeeks.org/php-array_replace-function/)

array_replace()函数是 PHP 中的一个内置函数，它以逗号(，)分隔的数组列表作为参数，并替换第一个数组中在其他数组中具有相同键的所有值。根据以下规则进行更换:

*   如果第一个数组中的某个键也存在于第二个数组中，那么它在第一个数组中的值将被第二个数组中该键的值替换。
*   如果第二个数组中的某个键在第一个数组中不存在，那么它将在第一个数组中创建，并且它在第二个数组中的值将复制到第一个数组中。
*   如果第一个数组中的某个键不存在于任何后续数组中，则该键的值在第一个数组中保持不变。
*   数组按照传递给函数的顺序进行处理，因此，如果第一个数组的键出现在多个数组中，则其值将被最后一次出现的数组的值替换。

**语法**:

```
*array* array_replace ( $array1, $array2, ...., $arrayn )

```

**参数**:该函数接受数组列表作为参数。函数的第一个参数是要替换的数组。该函数的其余参数是其值将被复制到第一个数组中的数组。

**返回值**:该函数返回参数中第一个数组修改后形成的数组。

示例:

```
Input : $array1 = array("orange", "banana", "apple", "raspberry")
        $array2 = array(0 => "pineapple", 4 => "cherry")
        $array3 = array(0 => "grape")
        array_replace($array1, $array2, $array3)
Output : Array
        (
            [0] => grape
            [1] => banana
            [2] => apple
            [3] => raspberry
            [4] => cherry
        )

Input : $array1 = array("aim", "plan", "vision", "clarity")
        $array2 = array("word1" => "loneliness", "word2" => "happiness")
        $array3 = array(0 => "solitude")
        array_replace($array1, $array2, $array3)
Output : Array
        (
            [0] => solitude
            [1] => plan
            [2] => vision
            [3] => clarity
            [word1] => loneliness
            [word2] => happiness
        )

```

在第一个示例中，键 *0* 出现在两个数组中，因此其值被替换为最后出现的那个，即*葡萄*，而键 *4* 出现在第二个数组中，因此其值也被替换。
在第二个例子中，键 *0* 出现在第三个数组中，因此它的值在第一个数组中被替换。键*字 1* 和*字 2* 不在第一个数组中，因此它们与它们的值一起被添加到第一个数组中。

下面的程序说明了 PHP 中的 array_replace()函数:

**程序 1** :

```
<?php

// Array to be replaced
$array1 = array("orange", "banana", "apple", 
                                 "raspberry");

// arrays that will replace the values 
// in the first array
$array2 = array(0 => "pineapple", 4 => "cherry");
$array3 = array(0 => "grape");

$resArr = array_replace($array1, $array2, 
                                 $array3);

print_r($resArr);

?>
```

输出:

```
Array
(
    [0] => grape
    [1] => banana
    [2] => apple
    [3] => raspberry
    [4] => cherry
)

```

**程序 2** :

```
<?php

// Array to be replaced
$array1 = array("aim", "plan", "vision", "clarity");

// arrays that will replace the values 
// in the first array
$array2 = array("word1" => "loneliness", 
                  "word2" => "happiness");
$array3 = array(0 => "solitude");

$resArr = array_replace($array1, $array2, 
                                 $array3);

print_r($resArr);

?>
```

输出:

```
Array
(
    [0] => solitude
    [1] => plan
    [2] => vision
    [3] => clarity
    [word1] => loneliness
    [word2] => happiness
)

```

**参考**:
T3】http://php.net/manual/en/function.array-replace.php