# PHP|XML_GET_CURRENT_BYTE_INDEX()函数

> Original: [https://www.geeksforgeeks.org/php-xml_get_current_byte_index-function/](https://www.geeksforgeeks.org/php-xml_get_current_byte_index-function/)

**先决条件：**[XML 基础知识](https://www.geeksforgeeks.org/xml-basics/)

**XML_GET_CURRENT_BYTE_INDEX()函数**是 PHP 中的内置函数，用于返回 XML 解析器的字节索引。

**语法：**

```
*int* xml_get_current_byte_index( *resource* $parser)
```

**参数：**此函数接受必需的单个参数**$xml_parser**。 此参数指定要使用的 XML 解析器。

**返回值：**此函数成功时返回指定解析器的当前字节索引，失败时返回 False。

**注意：**此函数适用于 PHP 4.0.0 及更新版本。

下面的程序演示了 PHP 中的 XML_GET_CURRENT_BYTE_INDEX()函数：

**gfg.xml 文件(不匹配标签)：**

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

**输出：**

```
ERROR: Mismatched tag
Error Code: 76
Line: 7
Column: 13
Byte Index: 208

```

**geeks.xml 文件：**

```
<?xml version="1.0 encoding="utf-8"?>
<user>
    <username> user123 </username>
    <name> firstname lastname </name>
    <phone> +91-9876543210 </phone>
    <detail> I am John Doe. Live in Kolkata, India. </detail>
</user>
```

**。 ：**

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

**输出：**

```
ERROR: String not closed expecting " or '
Error Code: 34
Line: 1
Column: 36
Byte Index: 37

```

**参考：**[https://www.php.net/manual/en/function.xml-get-current-byte-index.php](https://www.php.net/manual/en/function.xml-get-current-byte-index.php)