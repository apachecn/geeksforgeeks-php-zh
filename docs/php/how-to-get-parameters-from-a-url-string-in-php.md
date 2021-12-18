# 如何在 PHP 中从一个 URL 字符串中获取参数？

> 原文:[https://www . geesforgeks . org/how-to-a-URL-string-in-PHP/](https://www.geeksforgeeks.org/how-to-get-parameters-from-a-url-string-in-php/)

可以使用 pase_url()和 parse_str()函数在 PHP 中检索来自 URL 字符串的参数。

**注意:**页面 URL 和参数用**隔开？**性格。

[**parse_url()函数**](https://www.geeksforgeeks.org/php-parse_url-function/)**:**parse _ url()函数用于通过解析 url 来返回 URL 的组成部分。它解析一个网址，并返回一个包含其各种组件的关联数组。

**语法:**

```
parse_url( $url, $component = -1 )
```

[**parse_str()函数**](https://www.geeksforgeeks.org/php-parse_str-function/)**:**parse _ str()函数用于将查询字符串解析为变量。传递给此函数进行解析的字符串是通过网址传递的查询字符串的格式。

**语法:**

```
parse_str( $string, $array )
```

**方法:**使用 parse_url()函数解析 url 字符串，该函数将返回一个包含其(传递的 URL)各种组件的关联数组。parse_url()函数返回的数组查询，其中包含 url 的查询字符串。

下面的例子使用 parse_url()和 parse_str()函数从 url 字符串中获取参数。

**例 1:**

## PHP

```
<?php

// Initialize URL to the variable
$url = 'https://www.geeksforgeeks.org?name=Tonny';

// Use parse_url() function to parse the URL
// and return an associative array which
// contains its various components
$url_components = parse_url($url);

// Use parse_str() function to parse the
// string passed via URL
parse_str($url_components['query'], $params);

// Display result
echo ' Hi '.$params['name'];

?>
```

**输出:**

```
Hi Tonny
```

**例 2:**

## PHP

```
<?php

// Initialize URL to the variable
$url = 'https://www.geeksforgeeks.org/register?name=Amit&email=amit1998@gmail.com';

// Use parse_url() function to parse the URL
// and return an associative array which
// contains its various components
$url_components = parse_url($url);

// Use parse_str() function to parse the
// string passed via URL
parse_str($url_components['query'], $params);

// Display result
echo ' Hi '.$params['name'].' your emailID is '.$params['email'];

?>
```

**输出:**

```
Hi Amit your emailID is amit1998@gmail.com
```

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。