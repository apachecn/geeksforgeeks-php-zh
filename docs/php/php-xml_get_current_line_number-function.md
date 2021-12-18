# PHP|XML_GET_CURRENT_LINE_NUMBER()函数

> Original: [https://www.geeksforgeeks.org/php-xml_get_current_line_number-function/](https://www.geeksforgeeks.org/php-xml_get_current_line_number-function/)

**XML_GET_CURRENT_LINE_NUMBER()函数**是 PHP 中的一个内置函数，用于返回 XML 解析器的当前行号。

**语法：**

```php
*int* xml_get_current_line_number( *resource* $xml_parser )
```

**参数：**此函数接受所需的单个参数**$xml_parser**。 它指定要使用的 XML 解析器。
**返回值：**此函数成功时返回指定解析器的当前行号，失败时返回 False。

**注：**

*   此函数适用于 PHP 4.0.0 及更新版本。
*   这些示例可能在在线 IDE 上不起作用。 因此，尝试在本地服务器或 php 托管服务器上运行它。

加入时间：清华大学 2007 年 01 月 25 日下午 3：33

## 可扩展标记语言

```php
<?xml version="1.0" encoding="utf-8"?>
<user>
    <username> user123 </username>
    <name> firstname lastname </name>
    <phone> +91-9876543210 </phone>
    <detail> I am John Doe. Live in Kolkata, India. </detail>
</users>
```

## PHP

```php
<?php

// XML file containing mismatch tags
$xml_file = 'gfg.xml';

// XML parser initialization
$xml_parser = xml_parser_create();

// File opening in read mode
$file_pointer = fopen($xml_file, 'r');

// Reading data from the file stream
while ($xml_data = fread($file_pointer, 4096)) {

    // Parse the data chunk
    if(!xml_parse($xml_parser, $xml_data,
                        feof($file_pointer))) {

        // Displaying errors
        die( print "ERROR: " .

            // Error string
            xml_error_string(xml_get_error_code($xml_parser)) .

            "<br/>Error Code: " .

            // Error code
            xml_get_error_code($xml_parser) .

            "<br/>Line: " .

            // Line number where the error occurred
            xml_get_current_line_number($xml_parser) .

            "<br/>Column: " .

            // Column number where the error occurred
            xml_get_current_column_number($xml_parser) .

            "<br/>Byte Index: " .

            // Byte index where the current byte occurred
            xml_get_current_byte_index($xml_parser) . "<br/>"
        );
    }
}

// Free to XML parser
xml_parser_free($xml_parser);

?>
```

发帖主题：Re：Колибри0.7.0

```php
ERROR: Mismatched tag
Error Code: 76
Line: 7
Column: 13
Byte Index: 208
```

加入时间：清华大学 2007 年 01 月 25 日下午 3：33

## 可扩展标记语言

```php
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

```php
<?php

// XML file containing mismatch tags
$xml_file = 'geeks.xml';

// XML parser initialization
$xml_parser = xml_parser_create();

// File opening in read mode
$file_pointer = fopen($xml_file, 'r');

// Reading data from the file stream
while ($xml_data = fread($file_pointer, 4096)) {

    // Parse the data chunk
    if(!xml_parse($xml_parser, $xml_data,
                        feof($file_pointer))) {

        // Displaying errors
        die( print "ERROR: " .

            // Error string
            xml_error_string(xml_get_error_code($xml_parser)) .

            "<br/>Error Code: " .

            // Error code
            xml_get_error_code($xml_parser) .

            "<br/>Line: " .

            // Line number where the error occurred
            xml_get_current_line_number($xml_parser) .

            "<br/>Column: " .

            // Column number where the error occurred
            xml_get_current_column_number($xml_parser) .

            "<br/>Byte Index: " .

            // Byte index where the current byte occurred
            xml_get_current_byte_index($xml_parser) . "<br/>"
        );
    }
}

// Free to XML parser
xml_parser_free($xml_parser);

?>
```

发帖主题：Re：Колибри0.7.0

```php
ERROR: String not closed expecting " or '
Error Code: 34
Line: 1
Column: 36
Byte Index: 37
```

**引用：**[https://www.php.net/manual/en/function.xml-get-current-line-number.php](https://www.php.net/manual/en/function.xml-get-current-line-number.php)