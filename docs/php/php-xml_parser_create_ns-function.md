# PHP|xml_parser_create_ns()函数

> Original: [https://www.geeksforgeeks.org/php-xml_parser_create_ns-function/](https://www.geeksforgeeks.org/php-xml_parser_create_ns-function/)

**xml_parser_create_ns()函数**是 PHP 中的一个内置函数，用于创建具有名称空间支持的 XML 解析器，并返回资源句柄。

**语法：**

```
*resource* xml_parser_create_ns( *string* $encoding, *string* $separator )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Coding：**可选参数。 它指定字符编码
    *   对于 PHP 4 中的输入/输出
    *   仅适用于 PHP 5 的输出
    *   对于 5.0.0 和 5.0.1，默认输出字符集为 ISO-8859-1
    *   从 5.0.2 开始，默认输出字符集为 UTF-8
*   **$分隔符：**可选参数。 它指定标记名和命名空间的输出分隔符。 默认值为“：”。

**返回值：**

*   **成功时：**它返回要由其他一些 XML 函数使用的资源句柄。
*   **失败时：**返回 FALSE。

**注：**

*   此函数适用于 PHP 4.0.5 及更高版本。
*   这些示例可能在在线 IDE 上不起作用。 因此，尝试在本地服务器或 php 托管服务器上运行它。

下面的程序演示了 PHP 中的 xml_parser_create_ns()函数：

**程序 1：**

## PHP

```
<?php

// Create an XML parser with
// namespace support
$parser = xml_parser_create_ns();

// Free the xml parser
xml_parser_free($parser);

?>
```

发帖主题：Re：Колибри0.7.0

```
(no output)
```

**程序 2：**

## PHP

```
<?php

// Creating an XML parser
// with namespace support
$parser = xml_parser_create_ns();

// Free the xml parser
$res = xml_parser_free($parser);

// Check parser is created or not
if(!$parser) {
    echo "error occured!";
}else {
    echo "parser with namespace support has successfully been created";
}
?>
```

发帖主题：Re：Колибри0.7.0

```
parser with namespace support has successfully been created
```

**引用：**[https://www.php.net/manual/en/function.xml-parser-create-ns.php](https://www.php.net/manual/en/function.xml-parser-create-ns.php)