# PHP|XML_ERROR_STRING()函数

> Original: [https://www.geeksforgeeks.org/php-xml_error_string-function/](https://www.geeksforgeeks.org/php-xml_error_string-function/)

**先决条件：**[XML 基础](https://www.geeksforgeeks.org/xml-basics/)
**XML_ERROR_STRING()函数**是 PHP 中的内置函数，它返回生成的错误代码的 XML 解析器错误描述。

**语法：**

```
*string* xml_error_string( *int* $error_code)
```

**参数：**此函数接受必需的单个参数**$error_code**。 它指定由 xml_get_error_code()函数生成的 XML 解析器错误代码。

**返回值：**成功时返回 XML_GET_ERROR_CODE()生成的指定错误代码的 XML 解析器错误描述，失败时返回 FALSE。

**注意：**此函数适用于 PHP 4.0.0 及更新版本。

以下程序说明了 PHP 中的 xml_error_string()函数：
**gfg.xml 文件：**

## 可扩展标记语言

```
<?xml version="1.0" encoding="utf-8"?>
<user>
    <username> user123 </username>
    <name> firstname lastname </name>
    <phone> +91-9876543210 </phone>
    <detail> I am John Doe. Live in Kolkata, India. </detail>
</users>
```

**程序 1：**

## PHP

```
<?php

// Invalid XML file
$xml_file= 'gfg.xml';

// XML parser initialization
$xml_parser = xml_parser_create();

// Opening the file in read mode
$file_pointer = fopen($xml_file, 'r');

// Reading data from the file stream
while ($xml_data = fread($file_pointer, 4096)) {

    // Parsing the data chunk
    if (!xml_parse($xml_parser, $xml_data, feof($file_pointer))) {

        // Display error
        die( print "ERROR: " .

            // Error string
            xml_error_string(xml_get_error_code($xml_parser)) .

            "<br>Error Code: " .

            // Error code
            xml_get_error_code($xml_parser) .

            "<br>Line: " .

            // Line number where the error occurred   
            xml_get_current_line_number($xml_parser) .

            "<br>Column: " .

            // Column number where the error occurred   
            xml_get_current_column_number($xml_parser) .

            "<br>Byte Index: " .

            // Byte index where the current byte occurred
            xml_get_current_byte_index($xml_parser) . "<br>"
        );
    }
}

// Free to xml parser
xml_parser_free($xml_parser);

?>
```

发帖主题：Re：Колибри0.7.0

```
ERROR: Mismatched tag
Error Code: 76
Line: 7
Column: 13
Byte Index: 208
```

加入时间：清华大学 2007 年 01 月 25 日下午 3：33

## 可扩展标记语言

```
<?xml version="1.0 encoding="utf-8"?>
<user>
    <username> user123 </username>
    <name> firstname lastname </name>
    <phone> +91-9876543210 </phone>
    <detail> I am John Doe. Live in Kolkata, India. </detail>
</user>
```

**程序 2：**

## PHP

```
<?php

// Invalid XML file
$xml_file= 'geeks.xml';

// XML parser initialization
$xml_parser = xml_parser_create();

// Opening the file in read mode
$file_pointer = fopen($xml_file, 'r');

// Reading data from the file stream
while ($xml_data = fread($file_pointer, 4096)) {

    // Parsing the data chunk
    if (!xml_parse($xml_parser, $xml_data, feof($file_pointer))) {

        // Display error
        die( print "ERROR: " .

            // Error string
            xml_error_string(xml_get_error_code($xml_parser)) .

            "<br>Error Code: " .

            // Error code
            xml_get_error_code($xml_parser) .

            "<br>Line: " .

            // Line number where the error occurred   
            xml_get_current_line_number($xml_parser) .

            "<br>Column: " .

            // Column number where the error occurred   
            xml_get_current_column_number($xml_parser) .

            "<br>Byte Index: " .

            // Byte index where the current byte occurred
            xml_get_current_byte_index($xml_parser) . "<br>"
        );
    }
}

// Free to xml parser
xml_parser_free($xml_parser);

?>
```

发帖主题：Re：Колибри0.7.0

```
ERROR: String not closed expecting " or '
Error Code: 34
Line: 1
Column: 36
Byte Index: 37
```

**引用：**[https://www.php.net/manual/en/function.xml-error-string.php](https://www.php.net/manual/en/function.xml-error-string.php)