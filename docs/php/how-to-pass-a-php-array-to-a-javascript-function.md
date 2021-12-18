# 如何将一个 PHP 数组传递给一个 JavaScript 函数？

> 原文:[https://www . geesforgeks . org/how-pass-a-PHP-array-a-JavaScript-function/](https://www.geeksforgeeks.org/how-to-pass-a-php-array-to-a-javascript-function/)

通过使用 JavaScript 对象符号(JSON)，将 PHP 数组传递给 JavaScript 非常容易。

**方法 1:使用 json_encode()函数:**使用 **json_encode()** 函数返回值或数组的 json 表示。该函数可以采用一维和多维数组。

**步骤:**

*   在 PHP 中创建数组:

    ```php
    <?php
    $sampleArray = array(
            0 => "Geeks", 
            1 => "for", 
            2 => "Geeks", 
        );
    ?>

    ```

*   使用 json_encode()函数检索数组元素

    ```php
    var passedArray = <?php echo json_encode($sampleArray); ?>
    ```

**示例:**

```php
<?php

// Create an array
$sampleArray = array(
    0 => "Geeks", 
    1 => "for", 
    2 => "Geeks", 
)
?>

<script>

// Access the array elements
var passedArray = 
    <?php echo json_encode($sampleArray); ?>;

// Display the array elements
for(var i = 0; i < passedArray.length; i++){
    document.write(passedArray[i]);
}
</script>
```

**输出:**

```php
GeeksforGeeks
```

**方法二:使用 PHP 内爆()函数:**内爆()用于连接数组的元素。内爆()函数是 join()函数的别名，其工作原理与 join()函数完全相同。
内爆()函数用于构建一个字符串，该字符串在 JavaScript 中成为数组文字。因此，如果我们在 PHP 中有一个数组，我们可以将它传递给 JavaScript，如下所示:

```php
var passedArray = <?php echo '["' . implode('", "', $sampleArray) . '"]' ?>;

```

**示例:**

```php
<?php

// Creating a PHP Array
$sampleArray = array('Car', 'Bike', 'Boat');

?>

<script type="text/javascript">

// Using PHP implode() function
var passedArray = 
    <?php echo '["' . implode('", "', $sampleArray) . '"]' ?>;

// Printing the passed array elements
document.write(passedArray);

</script>
```

**输出:**

```php
Car, Bike, Boat
```

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。