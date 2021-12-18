# 通过值

搜索 PHP 多维数组

> Original: [https://www.geeksforgeeks.org/php-multidimensional-array-search-by-value/](https://www.geeksforgeeks.org/php-multidimensional-array-search-by-value/)

在 PHP 中，多维数组搜索是指在多级嵌套数组中搜索值。 有多种技术可以执行这种类型的搜索，例如迭代嵌套数组、递归方法和内置数组搜索函数。

**迭代方法：**
迭代数组并搜索有意义的匹配是可以遵循的最简单的方法。 检查给定数组的元素本身是否为数组，并将该元素添加到搜索路径，否则在嵌套数组上运行数组搜索。

**示例：**

```php
<?php
// PHP program to carry out multidimensional array search

// Function to iteratively search for a given value
function searchForId($search_value, $array, $id_path) {

    // Iterating over main array
    foreach ($array as $key1 => $val1) {

        $temp_path = $id_path;

        // Adding current key to search path
        array_push($temp_path, $key1);

        // Check if this value is an array
        // with atleast one element
        if(is_array($val1) and count($val1)) {

            // Iterating over the nested array
            foreach ($val1 as $key2 => $val2) {

                if($val2 == $search_value) {

                    // Adding current key to search path
                    array_push($temp_path, $key2);

                    return join(" --> ", $temp_path);
                }
            }
        }

        elseif($val1 == $search_value) {
            return join(" --> ", $temp_path);
        }
    }

    return null;
}

// Multidimensional array 
$gfg_array = array(
    array(
        'score' => '100',
        'name' => 'Sam',
        'subject' => 'Data Structures'
    ),
    array(
        'score' => '50',
        'name' => 'Tanya',
        'subject' => 'Advanced Algorithms'
    ),
    array(
        'score' => '75',
        'name' => 'Jack',
        'subject' => 'Distributed Computing'
    )
);

$search_path = searchForId('Advanced Algorithms',
                    $gfg_array, array('{content}apos;));

print($search_path);

?>
```

**Output:**

```php
$ --> 1 --> subject

```

**递归方法：**
以防嵌套数组级别增加时，编写此类程序并对其进行调试变得困难。 在这种情况下，最好编写一个递归程序，该程序无需添加任何嵌套的 for 循环即可干净地编写。

**示例：**

```php
<?php
// PHP program to carry out multidimensional array search

// Function to recursively search for a given value
function array_search_id($search_value, $array, $id_path) {

    if(is_array($array) && count($array) > 0) {

        foreach($array as $key => $value) {

            $temp_path = $id_path;

            // Adding current key to search path
            array_push($temp_path, $key);

            // Check if this value is an array
            // with atleast one element
            if(is_array($value) && count($value) > 0) {
                $res_path = array_search_id(
                        $search_value, $value, $temp_path);

                if ($res_path != null) {
                    return $res_path;
                }
            }
            else if($value == $search_value) {
                return join(" --> ", $temp_path);
            }
        }
    }

    return null;
}

// Multidimensional (Three dimensional) array
$gfg_array = array(
    "school1" => array(
        "year" => "2017",
        "data" => array(
            'score' => '100',
            'name' => 'Sam',
            'subject' => 'Data Structures'
        )
    ),

    "school2" => array(
        "year" => "2018",
        "data" => array(
            'score' => '50',
            'name' => 'Tanya',
            'subject' => 'Advanced Algorithms'
        )
    ),

    "school3" => array(
        "year" => "2018",
        "data" => array(
            'score' => '75',
            'name' => 'Jack',
            'subject' => 'Distributed Computing'
        )
    )
);

$search_path = array_search_id('Jack', $gfg_array, array('{content}apos;));
print($search_path);

?>
```

**Output:**

```php
$ --> school3 --> data --> name

```

**使用[array_search()](https://www.geeksforgeeks.org/php-array_search-function/)方法进行多维数组搜索：**
[array_search()](https://www.geeksforgeeks.org/php-array_search-function/)是一个内置函数，用于搜索与给定数组列/键相关的给定值。 此函数仅返回关键字索引，而不返回搜索路径。

**示例：**

```php
<?php
// PHP program to carry out multidimensional array search

// Multidimensional array
$gfg_array = array(
    array(
        'score'   => '100',
        'name'    => 'Sam',
        'subject' => 'Data Structures'
    ),
    array(
        'score'   => '50',
        'name'    => 'Tanya',
        'subject' => 'Advanced Algorithms'
    ),
    array(
        'score'   => '75',
        'name'    => 'Jack',
        'subject' => 'Distributed Computing'
    )
);

$id = array_search('50', array_column($gfg_array, 'score'));
echo $id;

?>
```

**Output:**

```php
1

```

PHP 是一种专门为 Web 开发设计的服务器端脚本语言。 您可以按照这个[PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和[PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。