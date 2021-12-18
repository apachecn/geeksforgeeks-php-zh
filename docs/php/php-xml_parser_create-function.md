# PHP|xml_parser_create()函数

> Original: [https://www.geeksforgeeks.org/php-xml_parser_create-function/](https://www.geeksforgeeks.org/php-xml_parser_create-function/)

函数的作用是：**xml_parser_create()函数**是 PHP 中的内置函数，用于创建 XML 解析器。

**语法：**

```php
*resource* xml_parser_create( *string* $encoding )
```

**参数：**此函数接受可选的单个参数**$coding**。 它指定字符编码：

*   对于 PHP 4 中的输入/输出
*   仅适用于 PHP 5 的输出
*   对于 5.0.0 和 5.0.1，默认输出字符集为 ISO-8859-1
*   从 5.0.2 开始，默认输出字符集为 UTF-8

**返回值：**此函数在成功时返回资源处理程序，如果成功则返回 False，如果失败则返回 False。

**注：**

*   此函数适用于 PHP 4.0.0 及更新版本。
*   这些示例可能在在线 IDE 上不起作用。 因此，尝试在本地服务器或 php 托管服务器上运行它。

加入时间：清华大学 2007 年 01 月 25 日下午 3：33

## 超文本标记语言

```php
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

```php
<?php

// Create an XML parser
$parser = xml_parser_create();

// set the character handler function
// for the XML parser
xml_set_character_data_handler($parser, "char_print");

// Opening the xml file
$filePointer = fopen("gfg.xml", "r");

// Reading xml data from file
while($data = fread($filePointer, 4096)) {

    // Parsing XML data
    xml_parse($parser, $data, feof($filePointer)) or

    // Display error when parse error occurs
    die(sprintf("XML Error: %s at line %d",

        // Error string
        xml_error_string(xml_get_error_code($parser)),

        // Current line
        xml_get_current_line_number($parser))
    );
}

// Free to xml parser
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

加入时间：清华大学 2007 年 01 月 25 日下午 3：33

## 可扩展标记语言

```php
<?xml version="1.0" encoding="utf-8"?>
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

// Creating an XML parser
$parser = xml_parser_create();

// Element handler function named "starting_handler"
// enables custom manipulation for output
function starting_handler($parser,
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
function ending_handler($parser, $element_name) {
    echo "<br>";
}

// Character handler funtion named "char_handler"
function char_handler($parser, $data) {
    echo $data;
}

// Setting the element handlers
xml_set_element_handler($parser,
            "starting_handler", "ending_handler");

// Setting character data handler
xml_set_character_data_handler($parser, "char_handler");

// Opening xml file
$fp = fopen("geeks.xml", "r");

// Reading xml file
while ($data = fread($fp, 4096)) {

    xml_parse($parser, $data, feof($fp)) or

    // Display error while xml parsing
    die (sprintf("XML Error: %s at line %d",

        // Error string
        xml_error_string(xml_get_error_code($parser)),

        // Error line number
        xml_get_current_line_number($parser))
    );
}

// Free to xml parser
xml_parser_free($parser);

// Closing file stream
fclose($fp);

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

**引用：**[https://www.php.net/manual/en/function.xml-parser-create.php](https://www.php.net/manual/en/function.xml-parser-create.php)