# 如何在 PHP 中合并多维数组中的重复值？

> 原文:[https://www . geesforgeks . org/如何合并多维数组中的重复值 php/](https://www.geeksforgeeks.org/how-to-merge-the-duplicate-value-in-multidimensional-array-in-php/)

要在 PHP 中合并多维数组中的重复值，首先，创建一个包含最终结果的空数组。然后我们遍历数组中的每个元素，并通过与其他元素进行比较来检查它的欺骗性。如果发现重复，那么首先合并重复的元素，然后将其推送到最终的数组，否则直接推送到最终的数组。
下面的例子以更显著的方式说明了上述方法:
**例子 1:** 在这个例子中，表里不一不超过两个。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
$arr = array(
    array('Roll'=>43, 'name'=>'Geeeks', 'subject'=>'Course-011'),
    array('Rool'=>38, 'name'=>'Gfg', 'subject'=>'Course-012'),
    array('Rool'=>43, 'name'=>'Geeks', 'subject'=>'Course-011')
);

// Create an empty array
$myarray = array();

// It returns the keys of the array
$keys = array_keys($arr);

// Iterating through the multidimensional array
for($i = 0; $i < count($arr); $i++) {

    $keys = array_keys($arr);

    // Iterating through each element in array
    foreach($arr[$keys[$i]] as $key => $value) {
        $f = 0;

        for($j = 0; $j < count($arr); $j++) {

            if($i != $j) {
                foreach($arr[$keys[$j]] as $key1 => $value1) {

                    // Checking for duplicacy
                    if(($key1 == $key) && ($value == $value1)) {
                        $f = 1;

                        // String index where the duplicate
                        // array exists
                        $dup_ind = $j;
                    }
                }
            }
        }
    }

    // If duplicate is found
    if($f ==1 ) {
        $temp_arr = array();
        array_push($temp_arr, $arr[$i]);

        // Merge both the arrays
        array_push($temp_arr, $arr[$dup_ind]);

        // Remove the duplicate element from original array
        unset($arr[$dup_ind]);

        // Finally push in the result array
        array_push($myarray, $temp_arr);
    }
    else {

        // Directly push in the result array
        array_push($myarray, $arr[$keys[$i]]);
    }
}

print_r($myarray);

?>
```

**输出:**

```php
Array
(
    [0] => Array
        (
            [0] => Array
                (
                    [Roll] => 43
                    [name] => Geeeks
                    [subject] => Course-011
                )

            [1] => Array
                (
                    [Rool] => 43
                    [name] => Geeks
                    [subject] => Course-011
                )

        )

    [1] => Array
        (
            [Rool] => 38
            [name] => Gfg
            [subject] => Course-012
        )

)
```

**示例 2:** 在本示例中，重复字段多于两个。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$arr = array(
    array('Roll'=>43, 'name'=>'Geeks', 'subject'=>'Course-011'),
    array('Roll'=>38, 'name'=>'GFG', 'subject'=>'Course-011'),
    array('Roll'=>26, 'name'=>'GeeksforGeeks', 'subject'=>'Course-011'),
    array('Roll'=>31, 'name'=>'gfg', 'subject'=>'Course-012')
);

foreach($arr as $k => $v) {
    $new_arr[$v['subject']][]=$v;
}

print_r($new_arr);

?>
```

**输出:**

```php
Array
(
    [Course-011] => Array
        (
            [0] => Array
                (
                    [Roll] => 43
                    [name] => Geeks
                    [subject] => Course-011
                )

            [1] => Array
                (
                    [Roll] => 38
                    [name] => GFG
                    [subject] => Course-011
                )

            [2] => Array
                (
                    [Roll] => 26
                    [name] => GeeksforGeeks
                    [subject] => Course-011
                )

        )

    [Course-012] => Array
        (
            [0] => Array
                (
                    [Roll] => 31
                    [name] => gfg
                    [subject] => Course-012
                )

        )

)
```