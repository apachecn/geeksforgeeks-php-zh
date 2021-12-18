# 如何用 PHP Regex 获取 YouTube 视频 ID？

> 原文:[https://www . geesforgeks . org/how-to-YouTube-video-id-with-PHP-regex/](https://www.geeksforgeeks.org/how-to-get-youtube-video-id-with-php-regex/)

YouTube ID 是一个由 11 个字符组成的字符串，由大写字母和小写字母以及数值组成。它被用来唯一地定义一个 YouTube 视频。任何 YouTube 视频的链接都由查询格式的 YouTube ID 组成，其变量通常写为“v”或“vi”，或者可以表示为“youtu.be/”。
来自以下链接的 YouTube ID 示例:

*   [https://youtu . be/hjgd 08 xfg9c](https://youtu.be/hjGD08xfg9c)
*   [https://www.youtube.com/watch?v=hjGD08xfg9c](https://www.youtube.com/watch?v=hjGD08xfg9c)
*   [https://www.youtube.com/watch?vi=hjGD08xfg9c](https://www.youtube.com/watch?vi=hjGD08xfg9c)
*   [https://www.youtube.com/？v=hjGD08xfg9c](https://www.youtube.com/?v=hjGD08xfg9c)
*   [https://www.youtube.com/？vi=hjGD08xfg9c](https://www.youtube.com/?vi=hjGD08xfg9c)

在所有这些 URL 中，字符串“hjGD08xfg9c”是 YouTube ID。现在利用这些知识，可以构建一个正则表达式，用于从 PHP 中的给定链接中获取 YouTube 标识。
**Regex:** 现在我们知道有五种基本格式可以获得 YouTube ID，即通过 v=或 vi=或 v/或 vi/或 YouTube.。那么查询从什么开始呢或者“yout.be/”，用“？”开始正则表达式或者寻找“yout.be/”。它会忽略之前的网址部分吗？或“yout.be/”。然后搜索“v=”或“vi=”，存储下 11 个字符并打印出来。
按照这个逻辑，正则表达式将是

```php
preg_match_all("#(?<=v=|v\/|vi=|vi\/|youtu.be\/)[a-zA-Z0-9_-]{11}#", $url, $match);
```

**示例:**该示例将显示 YouTube ID，其中输入将是指向 YouTube 的链接。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
$url = 'https://youtu.be/hjGD08xfg9c
```

**Output:** 

```php
Array
(
    [0] => hjGD08xfg9c
    [1] => hjGD08xfg9c
    [2] => hjGD08xfg9c
    [3] => hjGD08xfg9c
    [4] => hjGD08xfg9c
)
```

**备选:**我们可以使用两个函数来访问变量或查询，这两个函数是 [parse_str()](https://www.geeksforgeeks.org/php-parse_str-function/) 和 [parse_url()](https://www.geeksforgeeks.org/php-parse_url-function/) 。parse_str()将 parse_url()和一个输出变量作为参数，并将 url 的所有查询值放入输出变量中。parse_url()接受字符串格式的 url 和一个整数值，并根据传递的整数值返回 url 中不同属性的列表。
**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Store the URL into variable
$url = 'https://www.youtube.com/watch?v=hjGD08xfg9c';
$url1='https://www.youtube.com/?vi=hjGD08xfg9c';

// Use parse_str() function to parse the query string
parse_str( parse_url( $url, PHP_URL_QUERY ), $youtube_id_v );
parse_str( parse_url( $url1, PHP_URL_QUERY ), $youtube_id_vi );

// Display the output
echo $youtube_id_v['v'] . "\n";
echo $youtube_id_vi['vi'];

?>
```

**Output:** 

```php
hjGD08xfg9c
hjGD08xfg9c
```