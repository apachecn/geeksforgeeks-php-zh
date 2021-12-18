# PHP|XML_SET_CHARACTER_DATA_HANDLER()函数

> Original: [https://www.geeksforgeeks.org/php-xml_set_character_data_handler-function/](https://www.geeksforgeeks.org/php-xml_set_character_data_handler-function/)

**XML_SET_CHARACTER_DATA_HANDLER()函数**是 PHP 中的内置函数，用于设置 XML 解析器的字符数据处理函数。

**语法：**

```
*bool* xml_set_character_data_handler( *resource* $xml_parser, *callable* $data_handler )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$xml_parser：**它是必需的参数。 它保存了 XML 解析器的引用来设置字符数据处理程序。
*   **$DATA_HANDLER：**它是必需的参数。 它是一个包含函数名称的字符串。

```
handler( *resource* $parser, *string* $data )
```

处理程序函数必须具有以下两个参数：

*   **$xml_parser：**它保存调用处理程序的 XML 解析器的引用。
*   **$data：**它将字符数据保存为字符串。

**返回值：**此函数成功时返回 True，失败时返回 False。

**注：**

*   此函数适用于 PHP 4.0.0 及更新版本。
*   这些示例可能在在线 IDE 上不起作用。 因此，尝试在本地服务器或 php 托管服务器上运行它。

加入时间：清华大学 2007 年 01 月 25 日下午 3：33

## 可扩展标记语言

```
<?xml version="1.0" encoding="utf-8"?>
<user>
    <username> user123 </username>
    <name> firstname lastname </name>
    <phone> +91-9876543210 </phone>
    <detail> I am John Doe. Live in Kolkata, India. </detail>
</user>
```

**程序 1：**

## PHP

```
<?php

// Create an XML parser
$xml_parser = xml_parser_create();

// Set the character handler function for XML parser
xml_set_character_data_handler($xml_parser, "char_print");

// Opening xml file
$file_pointer = fopen("gfg.xml", "r");

// Reading xml data from file
while($data = fread($file_pointer, 4096)) {

    // Parsing XML data
    xml_parse($xml_parser, $data, feof($file_pointer)) or

    // Display error when parsing error occurs
    die (sprintf("XML Error: %s at line %d",

        // Error string
        xml_error_string(xml_get_error_code($xml_parser)),

        // Current line
        xml_get_current_line_number($xml_parser)));
}

// Free to xml parser
xml_parser_free($xml_parser);

fclose($file_pointer);

// Character handler function for XML parser
function char_print($xml_parser, $data_to_print) {
    echo $data_to_print;
}

?>
```

发帖主题：Re：Колибри0.7.0

```
user123 
firstname lastname 
+91-9876543210 
I am John Doe. Live in Kolkata, India. 
```

**程序 2：**

## PHP

```
<?php

// Create an xml parser
$xml_parser = xml_parser_create();

// Element handler function named "starting_handler"
// enables custom manipulation for output
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
function char_handler($xml_parser, $data) {
    echo $data;
}

// Setting element handlers
xml_set_element_handler($xml_parser,
        "starting_handler", "ending_handler");

// Setting character data handler
xml_set_character_data_handler($xml_parser, "char_handler");

// Opening xml file
$file_pointer = fopen("gfg.xml", "r");

// Reading xml file
while ($data = fread($file_pointer, 4096)) {
    xml_parse($xml_parser, $data, feof($file_pointer)) or

    // Display error while xml parsing
    die (sprintf("XML Error: %s at line %d",

        // Error string
        xml_error_string(xml_get_error_code($xml_parser)),

        // Error line number
        xml_get_current_line_number($xml_parser)));
}

// Free to xml parser
xml_parser_free($xml_parser);

// Closing file stream
fclose($file_pointer);

?>
```

发帖主题：Re：Колибри0.7.0

```
USER DATA
Username: user123
Name: firstname lastname
Phone no: +91-9876543210
More about user: I am John Doe. Live in Kolkata, India.
```

**引用：**[https://www.php.net/manual/en/function.xml-set-character-data-handler.php](https://www.php.net/manual/en/function.xml-set-character-data-handler.php)