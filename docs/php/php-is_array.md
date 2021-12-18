# PHP|is_array()函数

> Original: [https://www.geeksforgeeks.org/php-is_array/](https://www.geeksforgeeks.org/php-is_array/)

**is_array()**是[PHP](https://www.geeksforgeeks.org/php/)中的内置函数。 **is_array()**函数用于检查变量是否为数组。

**语法**：

```
*bool* is_array($variable_name)
```

**参数：**如上所述，此函数接受单个参数：
**$Variable_Name：**此参数保存我们要检查的变量。

**返回值**：它是一个布尔函数，因此当**$VARIABLE_NAME**为布尔值时返回 TRUE，否则返回 FALSE。

下面的示例演示了 PHP 中的**is_array()**函数。
**示例 1：**

```
<?php
// PHP code to demonstrate working of is_array()
$variable_name1=67.099;
$variable_name2=32;
$variable_name3="abc";
$variable_name4=array('A', 'B', 'C');

// $variable_name4 is an array, returns TRUE
if (is_array($variable_name4))
    echo "array('A', 'B', 'C') is an array . \n";
else
    echo "array('A', 'B', 'C') is not a array value. \n";

// $variable_name1 is not array, gives FALSE
if (is_array($variable_name1))
    echo "$variable_name1 is a array value. \n";
else
    echo "$variable_name1 is not a array value. \n";

// $variable_name2 is not array, gives FALSE
if (is_array($variable_name2))
    echo "$variable_name2 is a array value. \n";
else
    echo "$variable_name2 is not a array value. \n";

// $variable_name3 is not array, gives FALSE
if (is_array($variable_name3))
    echo "$variable_name3 is a array value. \n";
else
    echo "$variable_name3 is not a array value. \n";
?>
```

**Output:**

```
array('A', 'B', 'C') is an array . 
67.099 is not a array value. 
32 is not a array value. 
abc is not a array value.

```

**参考**：[http://php.net/manual/en/function.is-array.php](http://php.net/manual/en/function.is-array.php)