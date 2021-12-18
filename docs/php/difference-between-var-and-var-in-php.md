# PHP 中$var 和$var 的区别

> 原文:[https://www . geesforgeks . org/var 和 var-in-php 的区别/](https://www.geeksforgeeks.org/difference-between-var-and-var-in-php/)

在 PHP 中， [$var](https://www.geeksforgeeks.org/php-var-keyword/) 用于存储整型、字符串、布尔型、字符型等变量的值。$var 是一个变量，$var 将变量的值存储在其中。

**有:**有

**语法:**

```php
$variable = value;
```

*   $变量是变量名
*   该值是变量的初始值。

**示例 1:** 本示例使用$，存储和显示值。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php 

       // String value
       $value1 = "hello Geeks";  

    // Display string value
    echo $value1; 
    echo "<br/>";

    // Boolean value
    $value2 = true;       

    // Display boolean value
    echo $value2;  
    echo "<br/>";

    // Integer value
    $value3 = 34;    

    // Display integer value
    echo $value3; 
    echo "<br/>";
?>
```

 **Output**

```php
hello Geeks<br/>1<br/>34<br/>
```

**$var:** $var 将$variable 的值存储在其中。

**语法:**

```php
$variable = "value";  
$variable = "new_value";
```

*   $variable 是值为的初始变量。
*   $variable 用于保存另一个值。

我们可以通过使用第一个变量的$值获得另一个值。

**示例 2:** PHP 程序演示$var。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php 

      // String value
      $value1 = "hello";  

       // Display string value
      echo $value1; 

      echo "\n";

      // Store another string in $var
      $value1 = "Hello php";

    // Access another string using
    // value of $var
      echo "$hello";
?>
```

**Output**

```php
hello
Hello php
```

**两者的区别:**变量 **$var** 用于存储变量的值，变量 **$val** 用于存储变量的引用。