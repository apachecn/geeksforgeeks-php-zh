# PHP 中的多维关联数组

> 原文:[https://www . geesforgeks . org/多维-关联-数组-in-php/](https://www.geeksforgeeks.org/multidimensional-associative-array-in-php/)

PHP 多维数组用于存储与常数值相反的数组。关联数组以键和值对的形式存储数据，其中键可以是整数或字符串。**多维关联数组**常用于以组关系存储数据。

**创建:**我们可以通过将包含一组键和值对的数组映射到父键来创建多维关联数组。
下面的程序演示了如何创建多维关联数组:

```php
<?php

$languages = array();

$languages['Python'] = array(
    "first_release" => "1991", 
    "latest_release" => "3.8.0", 
    "designed_by" => "Guido van Rossum",
    "description" => array(
        "extension" => ".py", 
        "typing_discipline" => "Duck, dynamic, gradual",
        "license" => "Python Software Foundation License"
    )
);

$languages['PHP'] = array(
    "first_release" => "1995", 
    "latest_release" => "7.3.11", 
    "designed_by" => "Rasmus Lerdorf",
    "description" => array(
        "extension" => ".php", 
        "typing_discipline" => "Dynamic, weak",
        "license" => "PHP License (most of Zend engine
             under Zend Engine License)"
    )
);

print_r($languages);

?>
```

**Output:**

```php
Array
(
    [Python] => Array
        (
            [first_release] => 1991
            [latest_release] => 3.8.0
            [designed_by] => Guido van Rossum
            [description] => Array
                (
                    [extension] => .py
                    [typing_discipline] => Duck, dynamic, gradual
                    [license] => Python Software Foundation License
                )

        )

    [PHP] => Array
        (
            [first_release] => 1995
            [latest_release] => 7.3.11
            [designed_by] => Rasmus Lerdorf
            [description] => Array
                (
                    [extension] => .php
                    [typing_discipline] => Dynamic, weak
                    [license] => PHP License (most of Zend engine
             under Zend Engine License)
                )

        )

)

```

**说明:**在上面的程序中，父索引是 Python 和 PHP。父键与一组具有常数值的键相关联。最后一个键，即每个父键的描述已经与该组键和常数值的另一个数组相关联。这里，Python 和 PHP 是 first_release、latest_release、designed _ by 和 description 的父键，而 description 是扩展、类型规范和许可证的父键。

**检索值:**我们可以使用以下方法检索多维数组的值:

1.  **Using key:** We can use key of the associative array to directly retrieve the data value.

    **示例:**

    ```php
    <?php

    $languages = array();

    $languages['Python'] = array(
        "first_release" => "1991", 
        "latest_release" => "3.8.0", 
        "designed_by" => "Guido van Rossum",
        "description" => array(
            "extension" => ".py", 
            "typing_discipline" => "Duck, dynamic, gradual",
            "license" => "Python Software Foundation License"
        )
    );

    print_r($languages['Python']['description']);
    echo $languages['Python']['latest_release'];

    ?>
    ```

    **Output:**

    ```php
    Array
    (
        [extension] => .py
        [typing_discipline] => Duck, dynamic, gradual
        [license] => Python Software Foundation License
    )
    3.8.0

    ```

2.  **使用 foreach 循环:**我们可以使用 foreach 循环来检索多维关联数组中关联的每个键的值。
    **例:**

    ```php
    <?php

    $languages = array();

    $languages['Python'] = array(
        "first_release" => "1991", 
        "latest_release" => "3.8.0", 
        "designed_by" => "Guido van Rossum",
        "description" => array(
            "extension" => ".py", 
            "typing_discipline" => "Duck, dynamic, gradual",
            "license" => "Python Software Foundation License"
        )
    );

    foreach ($languages as $key => $value) {
        echo $key . "\n";
        foreach ($value as $sub_key => $sub_val) {

            // If sub_val is an array then again
            // iterate through each element of it
            // else simply print the value of sub_key
            // and sub_val
            if (is_array($sub_val)) {
                echo $sub_key . " : \n";
                foreach ($sub_val as $k => $v) {
                    echo "\t" .$k . " = " . $v . "\n";
                }
            } else {
                echo $sub_key . " = " . $sub_val . "\n";
            }
        }
    }

    ?>
    ```

    **输出:**

    ```php
    Python
    first_release = 1991
    latest_release = 3.8.0
    designed_by = Guido van Rossum
    description : 
        extension = .py
        typing_discipline = Duck, dynamic, gradual
        license = Python Software Foundation License

    ```

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。