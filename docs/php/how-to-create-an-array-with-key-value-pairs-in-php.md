# 如何在 PHP 中创建带有键值对的数组？

> 原文:[https://www . geeksforgeeks . org/如何在 php 中创建带键值对的数组/](https://www.geeksforgeeks.org/how-to-create-an-array-with-key-value-pairs-in-php/)

PHP 为我们提供了一种特殊类型的数组，称为*关联数组*，它允许我们创建一个带有*键值对*的数组。创建*关联数组*的语法如下:

**语法 1:** 使用数组()构造函数

```
$arrayVariable = array(
    key1  => value1,
    key2 => value2,
    key3 => value3,
    ...
    keyN => valueN,
);

```

**语法 2:** 使用简写符号

```
$arrayVariable = [
    key1  => value1,
    key2 => value2,
    key3 => value3,
    ...
    keyN => valueN,
];

```

**注:**

1.  最后一个键值对后的逗号是可选的。
2.  *键*可以是整数或字符串类型。
3.  *值*可以是任何有效的类型。
4.  如果*键*的类型不是字符串或整数，将根据*键*的类型转换为字符串或整数。

**示例 1:** 使用数组()构造函数

```
<?php
$websites = array(
    "Facebook" => 
"Facebook, Inc. is an online social media and
 social networking service company.",
    "Twitter" => 
"Twitter is a microblogging and social networking service on 
which users post and interact with messages known as tweets.",
    "LinkedIn" => 
"LinkedIn is a business and employment-oriented service
 that operates via websites and mobile apps.");

$websites["Instagram"] = "Instagram is a photo and video-sharing 
social networking service owned by Facebook, Inc.";
foreach ($websites as $key => $value) {
    echo "<p>$key: $value <p>";
}
?>
```

**输出:**
![Associative Arrays in PHP](img/fd6db58397c7a8a19b2f7b7073ba3758.png)

**示例 2:** 使用速记符号

```
<?php
$websites = [
    "Facebook" => 
"Facebook, Inc. is an online social 
    media and social networking service company.",

    "Twitter" => "Twitter is a microblogging and social networking service 
    on which users post and interact with messages known as tweets.",

    "LinkedIn" => "LinkedIn is a business and 
    employment-oriented service that operates via websites and mobile apps."];

$websites[
    "Instagram"] = "Instagram is a photo and video-sharing 
    social networking service owned by Facebook, Inc.";
foreach ($websites as $key => $value) {
    echo "<p>$key: $value <p>";
}
?>
```

**输出:**
![Associative Arrays in PHP](img/fd6db58397c7a8a19b2f7b7073ba3758.png)