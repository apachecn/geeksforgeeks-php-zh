# PHP|Gmagick 查询格式()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-queryformats-function/](https://www.geeksforgeeks.org/php-gmagick-queryformats-function/)

**Gmagick：：queryFormats()函数**是 PHP 中的一个内置函数，用于获取 Gmagick 对象支持的格式。

**语法：**

```
*array* Gmagick::queryformats( *string* $pattern )
```

**参数：**此函数接受单个参数**$Pattern**，该参数保存正则表达式模式以检查是否支持某种格式。

**返回值：**此函数返回包含格式的数组值。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：queryformat()函数**：

**程序 1(获取所有格式)：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick();

// Get all formats
$formats = $gmagick->queryformats('*');

foreach ($formats as $format) {
    echo $format . "<br>";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2(检查是否支持某种格式)：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick();

// Get all formats
$formats = $gmagick->queryformats('*');

// Call the checker function
checkFormat('JPEG', $formats);
checkFormat('xyz', $formats);

// Checker function
function checkFormat($format, $formats)
{
    if (in_array($format, $formats)) {
        echo $format . ' is supported<br>';
    } else {
        echo $format . ' isn\'t supported<br>';
    }
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/gmagick.queryformats.php](https://www.php.net/manual/en/gmagick.queryformats.php)