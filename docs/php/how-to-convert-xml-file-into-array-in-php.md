# PHP 中如何将 XML 文件转换成数组？

> 原文:[https://www . geesforgeks . org/如何将 xml 文件转换为 php 数组/](https://www.geeksforgeeks.org/how-to-convert-xml-file-into-array-in-php/)

给定一个 XML 文档，任务是将一个 XML 文件转换成 PHP 数组。为了将 XML 文档转换成 PHP 数组，使用了下面列出的一些 PHP 函数:

*   **[file_get_contents()函数](https://www.geeksforgeeks.org/php-file_get_contents-function/):**file _ get _ contents()函数用于以字符串形式读取文件。此功能使用服务器支持的内存映射技术，因此通过使其成为读取文件内容的首选方式来提高性能。
*   **[simplexml_load_string()函数](https://www.geeksforgeeks.org/php-simplexml_load_string-function/) :** 有时候需要用 PHP 解析 xml 数据。有几种方法可以解析 XML 数据。SimpleXML 就是其中之一。解析 XML 文档意味着在 XML 文档中导航并返回相关的信息。目前，少数应用编程接口以 JSON 格式返回数据，但仍有大量网站以 XML 格式返回数据。因此，如果我们想充分利用现有的应用编程接口，我们必须精通解析 XML 文档。
*   **json_encode()函数:**json _ encode()函数用于对一个 json 字符串进行编码，并返回值的 JSON 表示形式。
*   **[json_decode()函数](https://www.geeksforgeeks.org/php-json_decode-function/):**json _ decode()函数用于解码一个 JSON 字符串。它将一个 JSON 编码的字符串转换成一个 PHP 变量。

**第一步:创建一个 XML 文件(可选):**创建一个需要转换成数组的 XML 文件。
T3

```
<?xml version='1.0'?>  
<firstnamedb>  
    <firstname name='Akshat'>  
        <symbol>AK</symbol>  
        <code>A</code>  
    </firstname>  
    <firstname name='Sanjay'>  
        <symbol>SA</symbol>  
        <code>B</code>  
    </firstname>
    <firstname name='Parvez'>  
        <symbol>PA</symbol>  
        <code>C</code>  
    </firstname>
</firstnamedb>
```

**第二步:将文件转换为字符串:** XML 文件将使用 file_get_contents()函数导入 PHP，该函数将整个文件作为字符串读取并存储到变量中。

**第三步:将字符串转换为对象:**将字符串转换为对象，这可以通过 PHP 的一些内置函数 simplexml_load_string()轻松完成。

**第四步:将对象转换为 json:**JSON _ encode()函数用于对一个 JSON 字符串进行编码，并返回值的 JSON 表示。

**第五步:解码 json 对象:**JSON _ decode()函数解码一个 JSON 字符串。它将一个 JSON 编码的字符串转换成一个 PHP 变量。

**示例:**

```
<?php

// xml file path
$path = "GFG.xml";

// Read entire file into string
$xmlfile = file_get_contents($path);

// Convert xml string into an object
$new = simplexml_load_string($xmlfile);

// Convert into json
$con = json_encode($new);

// Convert into associative array
$newArr = json_decode($con, true);

print_r($newArr);

?>
```

**输出:**
![](img/170c9f1301665737e3890f7a94ec4f47.png)