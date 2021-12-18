# PHP|xml_parse()函数

> Original: [https://www.geeksforgeeks.org/php-xml_parse-function/](https://www.geeksforgeeks.org/php-xml_parse-function/)

函数的作用是：**xml_parse()函数**是 PHP 的内置函数，用于解析 XML 文档。

**语法：**

```php
*int* xml_parse( *resource* $xml_parser, *string* $xml_data, *bool* $is_final )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$xml_parser：**它是必需的参数。 它指定要使用的 XML 解析器。
*   **$XML_DATA：**必选参数。 它指定要解析的数据。
*   **$IS_FINAL：**可选参数。 如果此参数的值设置为 True，则数据是此解析中发送的最后一段数据。

**返回值：**此函数成功时返回 True，失败时返回 False。

**注：**

*   此函数适用于 PHP 4.0.0 及更新版本。
*   这些示例可能在在线 IDE 上不起作用。 因此，尝试在本地服务器或 php 托管服务器上运行它。

加入时间：清华大学 2007 年 01 月 25 日下午 3：33

## 可扩展标记语言

```php
<?xml version="1.0" encoding="utf-8"?>
<user>
    <username>user123</username>
    <name>firstname lastname</name>
    <phone>+91-9876543210</phone>
    <detail>I am John Doe. Live in Kolkata, India.</detail>
</user>
```

**程序 1：**

## PHP

```php
<?php

// Create an XML parser
$parser = xml_parser_create();

// Set the character handler function
// for the XML parser
xml_set_character_data_handler($parser, "char_print");

// Opening xml file
$filePointer = fopen("gfg.xml", "r");

// Reading xml data from file
while ($data = fread($filePointer, 4096)) {

    // Parsing XML data
    xml_parse($parser, $data, feof($filePointer)) or

        // Display error when parse error occurs
        die (sprintf("XML Error: %s at line %d",

        // Error string
        xml_error_string(xml_get_error_code($parser)),

        // Current line       
        xml_get_current_line_number($parser)));
}

// Freeing xml parser
xml_parser_free($parser);

fclose($filePointer);

// Character handler function for XML parser
function char_print($parser, $data) {
    echo $data;
}

?>
```

发帖主题：Re：Колибри0.7.0

```php
user123 
firstname lastname 
+91-9876543210 
I am John Doe. Live in Kolkata, India. 
```

**程序 2：**

## PHP

```php
<?php

// Create an xml parser
$xml_parser = xml_parser_create();

// Element handler function named "starting_handler"
// enables custom manupulation for output
function starting_handler($xml_parser,
            $element_name, $element_attrs) {

    switch($element_name) {
        case "USER":
            echo "<u>USER DATA</u><br>";
            break;
        case "USERNAME":
            echo "Username: ";
            break;
        case "NAME":
            echo "Name: ";
            break;
        case "PHONE":
            echo "Phone no: ";
            break;
        case "DETAIL":
            echo "More about user: ";
    }
}

// Element handler function named "ending_handler"
function ending_handler($xml_parser, $element_name) {
    echo "<br>";
}

// Character handler function named "char_handler"
function char_handler($xml_parser, $xml_data) {
    echo $xml_data;
}

// Setting element handlers
xml_set_element_handler($xml_parser,
                "starting_handler", "ending_handler");

// Setting character data handler
xml_set_character_data_handler($xml_parser, "char_handler");

// Opening xml file
$file_pointer = fopen("gfg.xml", "r");

// Reading xml file
while ($xml_data = fread($file_pointer, 4096)) {

    xml_parse($xml_parser, $xml_data, feof($file_pointer)) or

    // Display error while xml parsing   
    die (sprintf("XML Error: %s at line %d",

        // Error string
        xml_error_string(xml_get_error_code($xml_parser)),

        // Error line number
        xml_get_current_line_number($xml_parser)));
}

// Free xml parser
xml_parser_free($xml_parser);

// Closing file stream
fclose($file_pointer);

?>
```

发帖主题：Re：Колибри0.7.0

```php
USER DATA
Username: user123
Name: firstname lastname
Phone no: +91-9876543210
More about user: I am John Doe. Live in Kolkata, India.
```

**引用：**[https://www.php.net/manual/en/function.xml-parse.php](https://www.php.net/manual/en/function.xml-parse.php)