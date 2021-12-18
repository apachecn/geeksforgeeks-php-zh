# 如何用 PHP 解析一个 JSON 文件？

> 原文:[https://www . geesforgeks . org/how-parse-a-JSON-file-in-PHP/](https://www.geeksforgeeks.org/how-to-parse-a-json-file-in-php/)

在本文中，我们将使用 [PHP 通过显示](https://www.geeksforgeeks.org/php-tutorials/) [JSON](https://www.geeksforgeeks.org/javascript-json/) 数据来解析 JSON 文件。 PHP 是一种用于处理数据的服务器端脚本语言。JSON 代表 JavaScript 对象符号。JSON 数据被写成名称/值对。

**语法:**

> {
> 【数据】:[{
> 【键】:【值】，
> 【键】:值，
> 【键 n】:【值】
> }，
> 。。。
> 。。。
> {
> “键”:“值”，
> “键”:值，
> “键 n”:“值”
> }]
> }

**示例:**学生详细信息的 JSON 符号如下。

> {
> 【学生】:[{
> 【姓名】:【斯拉凡】、
> 【滚】:7058、
> 【科目】:【爪哇】
> }、
> {
> 【姓名】:【Jyothika】、
> 【滚】:7059、
> 【科目】:【SAP】
> }]
> }

**优势:**

*   JSON 不使用结束标记。
*   JSON 是一种较短的格式。
*   JSON 读写速度更快。
*   JSON 可以使用数组。

**方法:**创建一个 JSON 文件，保存为 my_data.json，我们在文件中取了*学生*的数据。内容如下。

> {
> 【学生】:[{
> 【姓名】:【斯拉凡】、
> 【滚】:7058、
> 【科目】:【爪哇】
> }、
> {
> 【姓名】:【Jyothika】、
> 【滚】:7059、
> 【科目】:【SAP】
> }]
> }

使用[**file _ get _ contents()**](https://www.geeksforgeeks.org/php-file_get_contents-function/)函数将 JSON 文件读入 PHP。该函数用于将文件读入 PHP 代码。

**语法:**

> file_get_contents(路径，文件名)

*   *文件名*是文件名，*路径*是要检查的位置。

*   使用 [**json_decode()**](https://www.geeksforgeeks.org/php-json_decode-function/) 函数解码到 json 文件成数组显示出来。

它用于将 JSON 转换为数组。

**语法:**

> json_decode($json_object，true)

*   $json_object 是要读取的文件对象。

**PHP 代码:**以下是解析 JSON 文件的 PHP 代码。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Read the JSON file 
$json = file_get_contents('my_data.json');

// Decode the JSON file
$json_data = json_decode($json,true);

// Display data
print_r($json_data);

?>
```

**输出:**

```php
Array ( 
    [Student] => Array ( 
        [0] => Array ( 
            [Name] => Sravan 
            [Roll] => 7058 
            [subject] => java 
        ) 
        [1] => Array ( 
            [Name] => Jyothika 
            [Roll] => 7059 
            [subject] => SAP 
        ) 
    ) 
)

```