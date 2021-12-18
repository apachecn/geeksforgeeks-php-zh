# 如何用 PHP 格式化电话号码？

> 原文:[https://www . geesforgeks . org/how-format-phone-numbers-in-PHP/](https://www.geeksforgeeks.org/how-to-format-phone-numbers-in-php/)

在本文中，我们将学习如何使用 PHP 格式化电话号码。当我们需要存储电话号码时，我们存储格式化的电话号码。使用 PHP，我们可以轻松格式化电话号码。

**方法:**在本文中，我们将使用[**preg _ match()**](https://www.geeksforgeeks.org/php-preg_match-function/)**方法**来格式化电话号码。**我们可以用这个方法来格式化电话号码。该函数具有从字符串中查找指定模式的特殊特性。**

****PHP 代码:** 以下是使用 **preg_match()格式化电话号码的完整代码。****

## **PHP**

```
<?php

// Create a formatting function
function formatting($phone){

    // Pass phone number in preg_match function
    if(preg_match(
        '/^\+[0-9]([0-9]{3})([0-9]{3})([0-9]{4})$/', 
    $phone, $value)) {

        // Store value in format variable
        $format = $value[1] . '-' . 
            $value[2] . '-' . $value[3];
    }
    else {

        // If given number is invalid
        echo "Invalid phone number <br>";
    }

    // Print the given format
    echo("$format" . "<br>");
}

// Call the function
formatting("+02025550170");

formatting("+01677942758");
?>
```

**输出:**

```
202-555-0170
167-794-2758
```