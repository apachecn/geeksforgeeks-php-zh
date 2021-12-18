# PHP 中数组如何转换成字符串？

> 原文:[https://www . geesforgeks . org/如何在 php 中将数组转换为字符串/](https://www.geeksforgeeks.org/how-to-convert-array-to-string-in-php/)

我们给出了一个数组，任务是将数组元素转换成字符串。在本文中，我们使用两种方法将数组转换为字符串。

**方法 1:** [**使用内爆()函数:**](https://www.geeksforgeeks.org/php-implode-function/) 内爆()方法是 PHP 中的一个内置函数，用于连接数组的元素。内爆()方法是 [PHP | join()函数](https://www.geeksforgeeks.org/php-join-function/) 的别名，工作原理与 join()函数完全相同。

**语法:**

```
*string* implode($separator, $array)
```

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php  

// Declare an array 
$arr = array("Welcome","to", "GeeksforGeeks", 
    "A", "Computer","Science","Portal");  

// Converting array elements into
// strings using implode function
echo implode(" ",$arr);

?>
```

**输出:**

```
Welcome to GeeksforGeeks A Computer Science Portal
```

**方法二:** [**使用 json_encode()函数:**](https://www.geeksforgeeks.org/php-json_encode-function/)****json _ encode()函数**是 PHP 中的一个内置函数，用于将 PHP 数组或对象转换为 JSON 表示。
**语法:****

```
*string* json_encode( $value, $option, $depth )
```

****示例:****

## **服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**

```
<?php 

// Declare multi-dimensional array 
$value = array( 
    "name"=>"GFG", 
    array( 
        "email"=>"abc@gfg.com", 
        "mobile"=>"XXXXXXXXXX"
    ) 
); 

// Use json_encode() function 
$json = json_encode($value); 

// Display the output 
echo($json); 

?> 
```

****输出:****

```
{"name":"GFG","0":{"email":"abc@gfg.com","mobile":"XXXXXXXXXX"}}
```

**PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。**